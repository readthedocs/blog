Securing Build Processes
========================

We've recently introduced a new build container subsystem based on Docker, which should go
mostly unnoticed for users. We're still ironing out some bugs with the system,
so raise an issue on `our issue tracker`_ if you are noticing any new issues
with your project builds.

This new system is part of an over-due security update to help isolate arbitrary
code execution.  As Read the Docs has grown, protecting against arbitrary
execution was a rapidly concern.  This build isolation layer was
developed as part of readthedocs.com, where security concerns are paramount due
to private repository access. We've been testing it for roll out on the
community site since then, but hadn't committed to switching production build
servers over due to the number of possible side effects.

This immediate change was in response to a release yesterday outlining some
possible attack vectors when dealing with arbitrary code execution and Python.
We didn't want to delay the fix for any longer following this release, and
decided to deal with any lingering issues as soon as they came up.

We have no reason to believe that any users have been effected by the reported issue.
As a part of rolling out this new system,
we have provisioned new build servers.
We are also actively monitoring for any other possible issues.

.. _our issue tracker: https://github.com/rtfd/readthedocs.org/issues

How It Works
------------

Under the new system,
we provision a unique container for each build.
All build steps that depend on executing code (pip, Sphinx),
run inside that container.
The container has 10 minutes to complete it's build step,
and we kill it from the host machine after this if it hasn't completed.
There is a shared filesystem that only contains the project checkout and artifact directories,
and no access to any other build server files.

Our build servers are firewalled from our application and database servers,
so they have no ability to connect to them.
Communication is done over a task queue on a dedicated server.
To start a build,
the web servers put a build task in the queue which is read by the build server.
When a build is finished,
a task is inserted into the queue,
and web servers pull documentation from the build server to be served.
This communication with the task queue happens outside of the container.

Breaking out of this system requires a privilege escalation attack,
and the ability to break out of the container in order to access the outer build system.
The main cause of these issues is running user code.
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
of executing the code. We should be able to eventually completely remove the
necessity for running arbitrary to generate docs with this method.
We've been working for some time now on supporting this with `sphinx-autoapi`_,
but don't think it's an adequate solution for every Python project just yet.

Unfortunately, Epydoc is not a strong project for us to rely on currently, as
activity has winded down in the past years and it lacks Python 3 support.
We hope to resolve these issues soon,
or look to another solution like `pydoctor`_ that is actively maintained.

The other source of code execution is the `conf.py` file inside Sphinx.
We have also been working on `readthedocs-build`_,
which implements a ``readthedocs.yml`` file that will contain Sphinx configuration.
This will remove the last step to remove arbitrary execution in our environment.

.. _Epydoc: http://epydoc.sourceforge.net/
.. _pydoctor: https://github.com/twisted/pydoctor/
.. _sphinx-autoapi: https://github.com/rtfd/sphinx-autoapi
.. _readthedocs-build: https://github.com/rtfd/readthedocs-build/pull/6

For more
--------

Read the Docs is a community project,
so if you are interested in helping us with the above tasks,
we are always happy to have help.
Specifically if you are able to help with development of `sphinx-autoapi`_
or `readthedocs-build`_,
that would greatly increase the speed that we can migrate to those solutions.
Also,
if you are knowledgeable in ways of locking Docker down even more,
we would love to talk.

You can email us at <security@readthedocs.org> for any issues that might be security related.
Please do not file them in our public issue tracker.
