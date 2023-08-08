.. post:: August 8, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Drop support for "Use system packages"
======================================


Read the Docs used to pre-install common scientific Python packages like ``scipy``, ``numpy``, ``pandas``, ``matplotlib`` and others
at system level to speed up the build process.
However, with all the work done in the Python ecosystem and the introduction of "wheels",
these packages are a lot easier to install via ``pip install`` and these pre-installed packages are not required anymore.
If you have Apt package dependencies,
they can be installed with `build.apt_packages <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-apt-packages>`_.

With the introduction of our new "Ubuntu 20.04" and "Ubuntu 22.04" Docker images,
we stopped pre-installing these extra Python packages and we encouraged users to install and pin all their dependencies using a ``requirements.txt`` file.
We have already stopped supporting "use system packages" on these newer images.

**We are removing the "use system packages" feature on August 29th**.
Make sure you are installing all the required dependecies to build your project's documentation using a ``requirements.txt`` file and specifying it in your ``.readthedocs.yaml``.

Here you have an example of the section required on the ``.readthedocs.yaml`` configuration file:

.. code-block:: yaml

   python:
     install:
       - requirements: docs/requirements.txt


The content of ``docs/requirements.txt`` would be similar to::

    scipy==1.11.1
    numpy==1.25.2
    pandas==2.0.3
    matplotlib==3.7.2

Read more about this in our :doc:`introduction to Reproducible Builds <readthedocs:guides/reproducible-builds>` guide for more details.

Please, `contact us`_ and let us know any inconvenient you may have with this change.

.. _contact us: mailto:hello@readthedocs.org
