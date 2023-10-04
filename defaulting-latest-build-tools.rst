.. post:: August 24, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Enabling latest versions for Sphinx & Mkdocs builds
===================================================

We are announcing the deprecation of building with older documentation tool versions by default.

Historically, Read the Docs installed a specific version based on the date your project was created.
This caused odd issues where reimporting a project could change behavior, and caused users to continue using very old versions of build tools that weren't supported by their authors.
This was done to maintain backwards compatibility,
but our platform now has robust support for defining a build environment,
so we encourage you to pin your dependencies instead.

**Starting on October 3rd Read the Docs will install the latest available version of MkDocs and Sphinx by default**.
If you want to use a different version, you can do this by pinning your dependencies.

Sphinx example
--------------

Previously we were installing ``Sphinx 1.8``,
which is no longer supported.
You should pin a specific version so that your documentation builds are reproducible.

Example ``.readthedocs.yaml`` configuration file:

.. code-block:: yaml

  version: 2

  # Set the OS, Python version and other tools you might need
  build:
    os: ubuntu-22.04
    tools:
      python: "3.11"

   python:
     install:
       - requirements: docs/requirements.txt

The content of ``docs/requirements.txt`` would be similar to::

  sphinx==6.2.1
  sphinx-rtd-theme==1.2.2
  pillow==5.4.1
  mock==1.0.1
  commonmark==0.9.1
  recommonmark==0.5.0

Mkdocs example
--------------

Previously we were installing ``Mkdocs 0.17.3``,
which is no longer supported.
You should pin a specific version so that your documentation builds are reproducible.

Example ``.readthedocs.yaml`` configuration file:

.. code-block:: yaml

  version: 2

  # Set the OS, Python version and other tools you might need
  build:
    os: ubuntu-22.04
    tools:
      python: "3.11"

   python:
     install:
       - requirements: docs/requirements.txt

The content of ``docs/requirements.txt`` would be similar to::

  mkdocs==1.5.1

Reproducible builds
-------------------

We highly recommend pinning your dependencies so that you can ensure a working build environment across time and on different build servers.

You can learn more about this in our `reproducible builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`_ guide.

