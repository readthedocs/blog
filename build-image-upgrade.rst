.. post:: Feb 14, 2017
    :author: Anthony

Build Image Upgrades
====================

Starting this week, we'll be deploying a new default image for our documentation
build environments. This image will change the default Python versions that are
supported.

We aren't expecting any issues to arise from this change, but be sure to raise
any issues on `our issue tracker`_ if you notice any strange behavior. The new
build image supports Python ``2.7`` and Python ``3.5``, dropping support for
Python ``3.4``. If you require access to Python ``3.4``, we suggest you sign up
for access to our next beta image.

The next image for our build process is now being tested. This image will
support multiple versions of Python: ``2.7``, ``3.3``, ``3.4``, ``3.5``, and
``3.6``. Instead of relying on the distribution's versions of Python, multiple
versions are instead installed from source, using `pyenv`_.

If you'd like beta access to this build image for your projects, you can sign
up here:

.. admonition:: Update

    Users are now able to opt in to a build image that support Python 3.6,
    signing up for beta access is no longer required. For more information, see
    our blog post on :doc:`/python-36-support`

We are slowly moving project configuration to our `YAML configuration file`_,
``readthedocs.yml``. Access to specific versions of Python will only be
available using this configuration method, by specifying a `python.version`_
element.

.. _our issue tracker: https://github.com/rtfd/readthedocs.org/issues
.. _pyenv: https://github.com/yyuu/pyenv
.. _YAML configuration file: http://docs.readthedocs.io/en/latest/yaml-config.html
.. _python.version: http://docs.readthedocs.io/en/latest/yaml-config.html#python-version
