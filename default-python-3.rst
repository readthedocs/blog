.. post:: Feb 12, 2019
   :author: Anthony
   :tags: python

Defaulting New Projects to Python 3
===================================

New projects that are just getting started with Read the Docs will now use
Python 3 by default. While it is still possible to configure your project to use
Python 2.7 with :doc:`our configuration file <readthedocs:config-file/v2>`, we
think it's important to help push the Python ecosystem towards adopting Python 3.

Our default Python version is currently Python 3.7. Projects can also select
Python versions 3.6 and 3.5 using our default build image. We will eventually
remove support for building projects with Python versions 3.3 and 3.4, however
it is still possible to select a build image with support for either version.

To select a specific version of Python, other than our default, you can use our
configuration file to specify a Python version, using the
:ref:`readthedocs:config-file/v2:python.version` configuration option.

If your project does require Python version 3.3 or 3.4, you can only select
these versions if you also specify ``stable`` build image for your project's
:ref:`readthedocs:config-file/v2:build.image (legacy)` configuration option. As we
release new versions of our build image, this ``stable`` image will eventually
lose support for Python 3.3 and 3.4, so it's suggested that your project upgrade
to a supported version of Python.
