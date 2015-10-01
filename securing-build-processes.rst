.. post:: Sep 30, 2015
   :tags: security, containers
   :author: Anthony

Securing Build Processes
========================

We've recently introduced a new build container subsystem based on Docker to readthedocs.org, 
which should go mostly unnoticed for users. 
We're still ironing out some bugs with the system,
so raise an issue on `our issue tracker`_ if you are noticing any new issues
with your project builds.

This new system is part of an over-due security update to help isolate arbitrary
code execution.  As Read the Docs has grown, protecting against arbitrary
execution was a rapidly growing concern.  This build isolation layer was
developed as part of readthedocs.com, where security concerns are paramount due
to private repository access. We've been testing it for roll out on the
community site since then, but hadn't committed to switching production build
servers over due to the number of possible side effects.

This immediate change was in response to a `release`_ yesterday outlining some
possible attack vectors when dealing with arbitrary code execution and Python.
We didn't want to delay the fix for any longer following this release, and
decided to deal with any lingering issues as soon as they came up.

We have no reason to believe that any users have been effected by the reported issue.
As a part of rolling out this new system,
we have provisioned new build servers.
We are also actively monitoring for any other possible issues.

.. _our issue tracker: https://github.com/rtfd/readthedocs.org/issues
.. _release: http://alex.hyperiongray.com/posts/302352-pwn-the-docs

How It Works
------------

Under the new system,
we provision a unique container for each build.
All build steps that depend on executing code (setup.py, pip, Sphinx),
run inside that container as individual commands,
triggered from the host build server.
The container has 10 minutes to complete these build commands before we time out the
build and kill the container system.
A filesystem is shared from the host build server,
which only contains the project checkout and artifact directories.
The container has no other access to the build server filesystem.

Our host build servers are firewalled from our application and database servers,
so they have no ability to connect to them.
Communication is done over a task queue on a dedicated server.
To start a build,
the web servers put a build task in a queue which is read by the build servers.
The host build servers manage the container creation,
command execution inside the container,
and the reporting of command and command return via our API.
When a build is finished,
a task is inserted into the queue,
and web servers pull documentation from the build server to be served.
All communication with the task queue and API happens outside of the container,
with the container strictly acting as a mechanism for command execution.

Breaking out of this system requires a privilege escalation attack,
and the ability to break out of the container in order to access the outer build system.
All of these measures are required because our system runs user code.
To properly fix this situation,
we are working to remove arbitrary execution form our stack entirely.

Fixing Arbitrary Execution
--------------------------

Arbitrary execution is something that is difficult, if not impossible, for us to
avoid currently. It's built into Sphinx's ``autodoc`` system, which gives Sphinx such
a useful reference documentation implementation.

However, executing Python in order to evaluate docstrings is a broken pattern.
For our purposes, it requires installing project dependencies and executing the
code of each Python project on Read the Docs.  These are two steps that introduce a
substantial number of issues with usability and number of security concerns.

Ideally, using a project like `Epydoc`_ to help take place of ``autodoc`` would
be the best path forward. This takes the approach of parsing the code, instead
of executing the code. This avoids executing the ``setup.py`` on the project,
and installing any dependencies, which is where code execution currently happens.
We've been working for some time now on supporting this with `sphinx-autoapi`_,
but don't think it's an adequate solution for every Python project just yet.

Unfortunately, Epydoc is not a strong project for us to rely on currently, as
activity has winded down in the past years and it lacks Python 3 support.
Another project with the same focus is `pydoctor`_,
though work to implement Python 3 support is required there too.

The other source of code execution is the ``conf.py`` file inside Sphinx.
We have also been working on `readthedocs-build`_,
which implements a ``readthedocs.yml`` file that will move Sphinx configuration
into a non-executable format.
This will remove the last step to remove arbitrary execution in our environment.

.. _Epydoc: http://epydoc.sourceforge.net/
.. _pydoctor: https://github.com/twisted/pydoctor/
.. _sphinx-autoapi: https://github.com/rtfd/sphinx-autoapi
.. _readthedocs-build: https://github.com/rtfd/readthedocs-build/pull/6

For more
--------

Read the Docs is an open source project.
If you are interested in helping us with the above tasks,
we are always happy to have help.
Specifically if you are able to help with development of `sphinx-autoapi`_
or `readthedocs-build`_,
that would greatly increase the speed that we can migrate to those solutions.
Also,
if you are knowledgeable in ways of locking Docker down even more,
we would love to talk.

As always,
you can email us at security@readthedocs.org for any issues that might be security related.
