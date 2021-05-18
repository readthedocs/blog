.. post:: May 19, 2021
   :tags: feature, builders
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      We have deployed a long awaited feature:
      the ability to install custom operating system packages.

Install custom operating system packages (apt)
==============================================

We are thrilled to announce that now Read the Docs users
can declare custom operating system packages in their project configuration
that will get installed in our Ubuntu-based builders using ``apt``.
This has been a long awaited feature,
and we think it will simplify the configuration of many projects,
especially scientific ones.

Previous solutions
------------------

The Ubuntu images used by our builders
contain `lots of preinstalled system
packages <https://github.com/readthedocs/readthedocs-docker-images/blob/8e4f035c219307e30f5e3326c3c8271cee4f2631/Dockerfile#L15-L131>`_
that we ship to all the projects
to make the most common use cases possible.
This includes compilers, development headers of common libraries, and others.

However, on one hand this makes our images way bigger than necessary,
and it is still not enough to solve 100 % of the use cases.
Fortunately, Read the Docs has supported the `conda package
manager <https://docs.readthedocs.io/en/stable/guides/conda.html>`_
for a long time already,
and this has allowed users with special needs to add
any non-Python libraries they needed.
Still, interoperability between conda and pip is not perfect,
and for users that are not used to conda this could feel like a hack.

New ``apt_packages`` configuration
----------------------------------

To overcome all these problems, we have added a new configuration value,
``build.apt_packages``, that receive a list of APT packages
that will be installed in our Ubuntu-based images.
`Our configuration
documentation <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-apt-packages>`_
contains a simple example:

.. code-block:: yaml

   version: 2

   build:
     image: latest
     apt_packages:
       - libclang
       - cmake

(Notice that at the moment our images are based Ubuntu 18.04,
this will change in the near future)

And you can draw inspiration from some community projects that are using this feature already:

- `geoserver-rest`_, a Python library to interact with GeoServer, uses `apt_packages`
  to `install some GDAL and pycurl
  dependencies <https://github.com/gicait/geoserver-rest/blob/70ec799937b18ec7baed6fd3f7b2bf2f11dd8237/.readthedocs.yaml#L3-L12>`_.
- `UCX-Py`_, a Python interface for the low-level networking library UCX,
  `installs extra dependencies to temporarily work around upstream
  issues <https://github.com/rapidsai/ucx-py/blob/504ba8efecafaf48b5a2692113b8da70f8229721/.readthedocs.yml#L3-L6>`_.

We are happy that this feature is already being used
minutes after being deployed
and are looking forward to seeing more projects make use of it.

Remember you can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_ and `Ethical Ad Server
Changelog <https://ethical-ad-server.readthedocs.io/page/developer/changelog.html>`_.

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _geoserver-rest: https://geoserver-rest.readthedocs.io/
.. _UCX-Py: https://ucx-py.readthedocs.io/
