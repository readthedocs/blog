.. post:: May 31, 2023
   :tags: builders, deprecation
   :author: Manuel
   :location: BCN
   :category: Changelog

Migrate your project to ``.readthedocs.yaml`` configuration file v2
===================================================================

We are announcing the **deprecation of building without a configuration file** (``.readtehdocs.yaml``)
together with the deprecation of configuration file v1 as well.

Read the Docs *will soon start requiring* a ``.readthedocs.yaml`` configuration file
for all the projects to build their documentation successfully.
We will stop creating a default configuration file *behind the scenes*, making assumptions for your projects
and trying our best to make the builds succeed.

We plan to deploy these changes and **start failing builds without a configuration file on September 2023**.
This matches the period when ``urllib3`` `drops support for OpenSSL 1.1.1 <https://github.com/urllib3/urllib3/issues/2168>`_
which is OpenSSL version that Ubuntu 18.04 has installed and it's used when the project doesn't have a configuration file.

The main reason behind this decision is it's pretty hard to maintain a set of defaults that are useful
for the amount of users we have and the number of different tools they use to build documentation.
Even when the defaults we chose were useful for a period of time,
we found they were almost impossible to update to newer versions of dependencies
because doing so would break a lot of projects that weren't using a configuration file
and pinning their dependencies (e.g. OS, Python version, dependencies, etc).

If you have a project on Read the Docs that it's not using a ``.readthedocs.yaml`` configuration file,
**we strongly recommend you to create one as soon as possible** to avoid breaking builds once we deploy the changes.

Here you have a minimal template configuration file that you can copy and paste to use in your project.
With this config file your project should build successfully now
and will keep working fine once we deploy the changes in September 2023.

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


It's worth to mention there are some small differences between the defaults used before and this configuration file.
These differences may require some manual adjustment that you will figure if the first build after making these changes fails:

* Operating system is changed from Ubuntu 18.04 to Ubuntu 22.04
* The new Ubuntu 22.04 may not have all the same system dependencies installed.
  If you need an Ubuntu package that it's not installed in the system,
  you can use
  `build.apt_packages <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-apt-packages>`_
  to install it.
* Python version is changed from 3.7 to 3.11.
* Git submodules are not clonned.
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

Starting with this suggested ``.readthedocs.yaml`` configuration file and taking into account the differences,
you will be able to update your project to the new requirements now and don't worry about this breaking change.

Finally, in case you have some extra time,
we recommend you to pin your Python dependencies as well to avoid builds breaking by surprise when a new release of any of your dependencies is made.
You can read the guide `How to create reproducible builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`_ for this.


Get in touch with us `via our support`_
and let us know if you are unable to use a configuration file for any reason.

.. _via our support: https://readthedocs.org/support/
