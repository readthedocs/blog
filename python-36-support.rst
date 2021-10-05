.. post:: Mar 29, 2018
    :author: Anthony
    :tags: python

Python 3.6 Support
==================

A long time back, :doc:`we wrote about </build-image-upgrade>` started testing
a new build image that uses `pyenv`_ to support multiple versions of Python.
Until recently, we were selectively opting projects in to help test the new
image, but at the beginning of the year, we added a configuration option to
allow projects to opt in to using the new image before we make it the default
build image.

In the near future, this build image will be the default build image, but for
now, you can manually opt your project in using our
:doc:`YAML configuration file <readthedocs:config-file/v2>`.

What you need
-------------

In order to use Python 3.6, you need to select our ``latest`` build image, and
you need to select to use Python 3.6. The build image is controlled with the
:ref:`readthedocs:config-file/v2:build.image (legacy)` setting in the YAML config, and you can
set the Python version with the :ref:`readthedocs:config-file/v2:python.version`
setting.

Your project's ``readthedocs.yml`` file should contain::

    build:
        image: latest

    python:
        version: 3.6

If you run in to any problems building, you might also need to wipe your version
for now. We plan to have some of the issues switching Python versions and build
images resolved before making a move to a new build image.

As always, if you notice anything strange with your build, feel free to raise an
issue on `our issue tracker`_.

.. _pyenv: https://github.com/yyuu/pyenv
.. _our issue tracker: https://github.com/rtfd/readthedocs.org/issues
