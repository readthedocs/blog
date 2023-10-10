.. post:: August 24, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Changes to default project dependencies
=======================================

.. note::

   This post was updated on Oct 10 to reflect all of the changes to installed dependencies

We are announcing the deprecation of automatic installation of several key project dependencies,
and builds will no longer install older documentation tool versions by default.

Historically, Read the Docs installed a specific version of several dependencies based on the date your project was created.
This caused odd issues where reimporting a project could change behavior, and caused users to continue using very old versions of build tools that weren't supported by their authors.
This was done to maintain backwards compatibility,
but our platform now has robust support for defining a build environment,
so we encourage you to pin your dependencies instead.

**Starting on October 3rd default dependencies installed for each project build will change.**
If your project was previously depending on these default dependencies,
your project's builds may encounter errors or failures due to missing packages.

To resolve these build failures we recommend defining all of your project's dependencies.
See the examples below for guidance on how to update your project configuration
or learn more about managing dependencies in our `guide for reproducible builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`_.

The changes to default dependencies installed during the build process are:

.. list-table::
   :header-rows: 1
   :width: 100%
   :align: center
   :widths: 10, 5, 5

   - * Package
     * Prior version
     * New version
   - * Sphinx
     * ``1.8.5``
     * *Latest release*
   - * MkDocs
     * ``0.17.3``
     * *Latest release*
   - * ``sphinx-rtd-theme``
     * *Latest release*
     * *Not installed*
   - * ``recommonmark``
     * *Latest release*
     * *Not installed*
   - * ``commonmark``
     * *Latest release*
     * *Not installed*
   - * ``pillow``
     * *Latest release*
     * *Not installed*
   - * ``mock``
     * *Latest release*
     * *Not installed*

Sphinx example
--------------

If your project uses Sphinx to build its documentation,
you will need to install Sphinx and may need to install the ``sphinx-rtd-theme`` package.
Previously, Sphinx version ``1.8.5`` could have been the default version installed for your project,
which we do not recommend installing as it is no longer supported.

A basic configuration example to work from would include the following files:

.. code-block:: yaml
  :caption: .readthedocs.yaml

  version: 2

  # Set the OS, Python version and other tools you might need
  build:
    os: ubuntu-22.04
    tools:
      python: "3.11"

   python:
     install:
       - requirements: docs/requirements.txt

.. code-block::
  :caption: docs/requirements.txt

  sphinx==6.2.1
  sphinx-rtd-theme==1.2.2
  pillow==5.4.1
  mock==1.0.1
  commonmark==0.9.1
  recommonmark==0.5.0

MkDocs example
--------------

If your project uses MkDocs to build its documentation,
you will need to find the latest version of MkDocs that your project can use.

A basic configuration example to work from would include the following files:

.. code-block:: yaml
  :caption: .readthedocs.yaml

  version: 2

  # Set the OS, Python version and other tools you might need
  build:
    os: ubuntu-22.04
    tools:
      python: "3.11"

   python:
     install:
       - requirements: docs/requirements.txt

.. code-block::
  :caption: docs/requirements.txt

  mkdocs==1.5.1


.. This section is mostly to direct search results

Build errors
------------

Some of the errors you might encounter are from missing dependencies:

- ``ModuleNotFoundError: No module named 'sphinx_rtd_theme'``
- ``ModuleNotFoundError: No module named 'recommonmark'``

Or you might notice errors from backwards incompatible API changes on modern
releases of Sphinx, ``docutils``, and other packages:

- ``AttributeError: 'Module' object has no attribute 'doc'``
