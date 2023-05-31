.. post:: May 31, 2023
   :tags: builders, deprecation
   :author: Manuel
   :location: BCN
   :category: Changelog

Migrate your project to ``.readthedocs.yaml`` configuration file v2
===================================================================

We are announcing a new **requirement for all builds to use our configuration file version 2: ``.readthedocs.yaml``**.
This announcement deprecates builds without a configuration file, as well as version 1 of our configuration file.

Read the Docs *will start requiring* a ``.readthedocs.yaml`` configuration file
for all projects in order to build documentation successfully.
We will stop supporting builds without explicit configuration,
because this creates implicit dependencies that users aren't aware of.

**We plan to start failing builds not using configuration file version 2 on September 4, 2023**.
This matches the period when ``urllib3`` `drops support for OpenSSL 1.1.1 <https://github.com/urllib3/urllib3/issues/2168>`_
which is the OpenSSL version installed by the build image used when the project doesn't specify a configuration file.

The main reason behind this decision is that it's hard to maintain a set of defaults that are useful
for all of our users and the different tools they use to build documentation.
Without a configuration file, we must guess the configuration the project needs to build, which is difficult to do reliably.
Even if the defaults we chose worked well for a period of time,
we found it impossible to change over time.
Doing so would break projects that were relying on our defaults instead of specifying a configuration file
and pinning their dependencies (e.g. OS, Python version, dependencies, etc).

Deprecation timeline
--------------------

We understand this change will effect many of our users,
so we have a timeline to communicate this deprecation to our users effectively.

* **June 2023**: Email project owners with unsupported configurations once a week, along with an onsite notification to alert them of the deprecation.
* **Monday, July 24, 2023**: Do the first brownout (temporarily enforce this deprecation) for 2 hours in 3 timezones, 9:00-11:00, in 3 timezones: UTC-8, UTC, and UTC+8.  
* **Monday, August 7, 2023**: Do a second brownout (temporarily enforce this deprecation) for 2 hours in 3 timezones, 9:00-11:00, in 3 timezones: UTC-8, UTC, and UTC+8.  
* **Monday, September 4, 2023**: Fully remove support for building documentation without configuration file v2.

Adding a configuration file
---------------------------

If you have a project on Read the Docs that is not using a ``.readthedocs.yaml`` configuration file,
**you will need to create one as soon as possible** to continue building your project.

Below is a minimal configuration template that you can copy and paste into your project.
With this configuration file, your project should build successfully
and will continue building after we deprecate our default build configuration in September 2023.

.. code:: yaml

   # .readthedocs.yaml
   # Read the Docs configuration file
   # See https://docs.readthedocs.io/en/stable/config-file/v2.html for details

   # Required
   version: 2

   # Set the version of Python and other tools you might need
   build:
     os: ubuntu-22.04
     tools:
       python: "3.11"

   # Build documentation in the docs/ directory with Sphinx
   sphinx:
     configuration: docs/conf.py
     
   # We recommend specifying your dependencies to enable reproducible builds:
   # https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html
   # python:
   #   install:
   #   - requirements: docs/requirements.txt

Additional help
---------------

There are some small differences between our build defaults and this configuration file template above.
If you notice a build failure after making these changes,
here are some things you can check while you tune your ``.readthedocs.yaml`` file:

* The operating system has changed from Ubuntu 18.04 to Ubuntu 22.04
* The new Ubuntu 22.04 may not have all the same system dependencies installed.
  If you need an Ubuntu package that's not installed in the system,
  you can use
  `build.apt_packages <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-apt-packages>`_
  to install it.
* The default Python version has changed from 3.7 to 3.11.
* All the configuration done from the dashboard
  (:menuselection:`Project Admin --> Advanced Settings --> Default settings`)
  is ignored when using a configuration file. These settings have to be migrated to your project's configuration file.

  * ``Documentation type`` is now defined via
    `sphinx <https://docs.readthedocs.io/en/stable/config-file/v2.html#sphinx>`_ or
    `mkdocs <https://docs.readthedocs.io/en/stable/config-file/v2.html#mkdocs>`_,
    depending on which documentation tool your project is using.
  * ``Requirements file`` is now defined via
    `python.requirements <https://docs.readthedocs.io/en/stable/config-file/v2.html#requirements-file>`_.
  * ``Python Interpreter`` is now defined via
    `build.tools.python <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-tools-python>`_.
  * ``Install Project`` is now defined via
    `python.install <https://docs.readthedocs.io/en/stable/config-file/v2.html#python-install>`_.
  * ``Use system packages`` *is deprecated* in favor of declaring all your dependencies via a requirements file using
    `python.requirements <https://docs.readthedocs.io/en/stable/config-file/v2.html#requirements-file>`_.
  * ``Python configuration file`` is now defined via
    `sphinx.configuration <https://docs.readthedocs.io/en/stable/config-file/v2.html#sphinx-configuration>`_.

* Git submodules are not cloned automatically.
  You can tell Read the Docs to clone them by using
  `submodules.include <https://docs.readthedocs.io/en/stable/config-file/v2.html#submodules-include>`_
  config key.
* HTMLZip format is not built by default.
  In case you want to keep building it,
  you can use the config key
  `formats <https://docs.readthedocs.io/en/stable/config-file/v2.html#formats>`_.
* Node.js is not available by default.
  You can make it available by using
  `build.tools.nodejs <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-tools-nodejs>`_
  config key.

Starting with this suggested ``.readthedocs.yaml`` configuration file and taking into account these differences,
you should be able to define a working configuration file and avoid breaking changes in the future.


What's next?
------------

In case you have some extra time,
we recommend that you pin your project's Python dependencies as well.
This helps avoid surprise build errors when new packages are released.
You can find more information in our guide,
`How to create reproducible builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`_.


Contact us
----------

`Contact us`_ if you have any questions,
and let us know if you are having trouble using a configuration file for any reason.

.. _Contact us: https://readthedocs.org/support/
