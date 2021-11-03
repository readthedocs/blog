.. post:: November 2, 2021
    :tags: builders
    :author: Anthony
    :location: GEG

.. meta::
    :description lang=en:
        TBD

Build errors with docutils 0.18
===============================

Starting about a week ago, some users started reporting new errors with
their project builds. In most cases, these errors appeared out of nowhere and
are usually rather cryptic errors referencing `Sphinx`_ and `docutils`_.

So, what is happening?

These errors are due to an incompatibility bewteen old versions of `Sphinx`_ and
one of it's dependencies, `docutils`_. You probably have not directly interacted
with docutils, but this is the library that provides reStructuredText parsing to
both Sphinx and to the Python standard library documentation tooling.

There are a number of errors that users have reported due to this
incompatibility, but the most common error is:

.. code::

    TypeError: 'generator' object is not subscriptable

If your project's builds suddenly start failing with the above error message, or
other cryptic errors that don't seem related to your project, your project is
most likely encountering this bug.

.. _Sphinx: https://pypi.org/project/Sphinx/
.. _docutils: https://pypi.org/project/docutils/

Why is this happening?
----------------------

The underlying cause for this error is using an outdated version of `Sphinx`_
(version < 3.0) with the latest release of `docutils`_ (version 0.18,
released October 26). This latest release of docutils is no longer comptible
with Sphinx versions 1.x and 2.x, however these versions do not specify a upper
limit to the version of docutils installed, and so will install the latest
release by default.

Fixing the error
----------------

We'll be assisting the `Sphinx`_ and `docutils`_ maintainers to find a solution
that doesn't involve manual intervention, but for now we suggest you manually
resolve this issue for any of your projects that have encountered the bug.

There are two changes that will resolve this issue:

Upgrade `Sphinx`_ to version 3 or later
    We recommend this option for most users. If your project doesn't
    specifically still require Sphinx 1.x or 2.x, your project can most likely
    be upgraded, without issues, to a modern version of Sphinx. As a bonus,
    you'll be able to use the latest Sphinx releases and extensions that only
    support modern Sphinx releases.

    It is worth noting that one reason why you might still be using an old
    version of Sphinx is if you generate API documentation for Python 2
    compatible code. In this case, you'll have more work ahead of you in order
    to upgrade, as Sphinx version 3 and 4 only support Python 3.

Downgrade `docutils`_
    This is the next best option if you can't immediately upgrade Sphinx. If you
    are familiar with Python packaging, the best specifier to use is
    ``docutils<0.18``.

Fixing the error on Read the Docs
---------------------------------

If you aren't already, you should add a :doc:`configuration file <readthedocs:config-file/v2>`
for your project, so that you can specify additional dependencies to install at
build time. There are a few supported methods for installation, depending on how
you normally install dependencies for your project. If you are not currently
specifying any dependencies on Read the Docs, you most likely will want to use
the :ref:`python.install.requirements <readthedocs:config-file/v2:Requirements file>` configuration option.

.. seealso::
    :ref:`Read the Docs tutorial <readthedocs:tutorial/index:Customizing the build process>`
        An introduction to our configuration file and some basic usage examples

    :ref:`.readthedocs.yaml python.install options <readthedocs:config-file/v2:python.install>`
        All of the supported Python dependency installation options

    https://github.com/readthedocs/readthedocs.org/issues/8616
        An example stack trace of this bug and discussion around resolving the
        error
