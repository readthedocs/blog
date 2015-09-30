Securing Build Processes
========================

We've recently introduced a new build container subsystem, which should go
mostly unnoticed for users. We're still ironing out some bugs with the system,
so raise an issue on `our issue tracker`_ if you are noticing any new issues
with your project builds.

This new system is part of an over-due security update to help isolate arbitrary
code execution.  As Read the Docs has grown, protecting against arbitrary
execution was a rapidly growing concern.  This build isolation layer was
developed as part of readthedocs.com, where security concerns are paramount due
to private repository access. We've been testing it for roll out on the
community site since then, but hadn't committed to switching production build
servers over due to the number of possible side effects.

This immediate change was in response to a release yesterday outlining some
possible attack vectors when dealing with arbitrary code execution and Python.
We didn't want to delay the fix for any longer following this release, and
decided to deal with any lingering issues as soon as they came up.

Additionally, we've reprovisioned all new build servers and have been working to
lock down attack vectors that exist if a virtual machine is exploited and broken
out of. Isolating builds with individual virtual machines may be a next step,
but would be a strain on our already limited budget.

.. _our issue tracker: https://github.com/rtfd/readthedocs.org/issues

Arbitrary Execution
-------------------

Arbitrary execution is something that is difficult, if not impossible, for us to
avoid. It's built into Sphinx's ``autodoc`` system, which gives Sphinx such
a useful reference documentation implementation.

However, executing Python in order to evaluate docstrings is a broken pattern.
For our purposes, it requires installing project dependencies and executing the
code of each project on Read the Docs.  These are two steps that introduce a
substantial number of issues with usability and number of security concerns.

Ideally, using a project like `Epydoc`_ to help take place of ``autodoc`` would
be the best path forward. We might be able to eventually completely remove the
necessity for arbitrary code execution altogether with this method. This method
relies on parsing Python to pull docstrings out of code, not execution.
We've been working for some time now on supporting this with `sphinx-autoapi`_,
but don't think it's an adequate solution for every Python project just yet.

Unfortunately, Epydoc is not a strong project for us to rely on currently, as
activity has winded down in the past years and it lacks Python 3 support. We
haven't yet taken to maintaining it ourselves, but it is on our list.

.. _Epydoc: http://epydoc.sourceforge.net/
.. _sphinx-autoapi: https://github.com/rtfd/sphinx-autoapi

Changes
-------

Foremost, builds are now isolated in a minimal container system. All that exists
in these containers is your source code, your dependencies, and necessary third
party libraries and binaries to build documentation. Access to the code
checkouts and built documentation of other projects is not possible without
exploiting the machine to break out of the virtual machine. These systems don't
have access to any internal services, and are only used to encapsulate
individual build commands.

We are also addressing a number of performance issues by isolating the build
systems.  Running virtual machines for each build allows us to give more
granular access to system resources. Memory and CPU time are commonly over-used
by projects, which puts a significant strain on the build servers for projects
that commit often. These projects may find their builds are timing out, or are
being killed due to memory consumption.

We'll discus more about offering stronger build platforms to users that have an
active subscription to Read the Docs shortly. We would have liked to have this
in place before rolling out this build layer, so contact us if your project is
running into resource limits.

For more
--------

As always, for responsible disclosure, please email us at
<security@readthedocs.org> if you discover what you think is a security flaw.
