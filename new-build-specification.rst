.. post:: Oct 14, 2021
   :tags: feature, builders
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      You can now use a build image based on Ubuntu 20.04 on Read the Docs
      with some extra features.

Ubuntu 20.04, Python 3.10, and support for Node, Rust, and Go
=============================================================

We are excited to announce that now Read the Docs users
can use a newer build specification in their projects
that will change the base image to one based on Ubuntu 20.04,
ship the recently released Python 3.10,
and allow users to easily specify the version of Node.js, Rust, and Go.
This feature has been a long time in the making,
and we think it will simplify the configuration of many projects.

Previous situation
------------------

The Docker images used by our builders were based on Ubuntu 18.04.
Recently, we added a new feature to :doc:`install custom system packages </apt-packages>`,
which allowed many projects to have better control of their build process
without having to use conda to manage non-Python dependencies.

However, this Ubuntu version was released three years ago and,
even though it was good enough for most projects,
we have been receiving requests to upgrade certain system packages over the years.
Since these are managed through the operating system package manager,
and we do not provide a way to add custom Personal Package Archives,
such upgrades were not possible.

Many Python projects use a secondary programming language
for a variety of reasons. Established compiled languages like C, C++, and FORTRAN
have readily available compilers that will work for the majority of use cases.
However, other younger technologies move at a faster pace,
and developers often want specific versions of the toolchains
that cannot be installed with the system package manager.
This affected projects that combine backend and frontend code
that need Node.js to compile their JavaScript sources, such as Jupyter extensions,
and libraries with performance-critical code written in Rust or Go.

We have often suggested specifying custom versions of non-Python dependencies
`using conda <https://docs.readthedocs.io/en/stable/guides/conda.html>`_,
to specify custom versions of non-Python dependencies,
but this requires learning another tool that might be unfamiliar for some projects.

New ``build`` YAML configuration
--------------------------------

To overcome all these problems, we have added a new configuration value,
``build.tools``, that receive a dictionary of toolchain versions.
This new configuration requires specifying the base image name
in ``build.os``, currently ``ubuntu-20.04``.
:doc:`Our configuration documentation <readthedocs:config-file/v2>`
contains a simple example:

.. code-block:: yaml

   version: 2

   # Set the version of Python and other tools you might need
   build:
     os: ubuntu-20.04
     tools:
       python: "3.9"
       # You can also specify other tool versions:
       # nodejs: "16"
       # rust: "1.55"
       # golang: "1.17"

And you can draw inspiration from some community projects
that are using this feature already:

- `cryptography`_, the reference Python library for cryptographic algorithms,
  can now `specify the Rust version required to build the
  package <https://github.com/pyca/cryptography/blob/c3fcc6759a86bbd847e3da067152ee7d2b88c194/.readthedocs.yml#L10-L15>`_.
- `parsel`_, a Python library to manipulate HTML and XML using XPath and CSS selectors,
  leverages the new specification to `build their documentation on the just released
  Python 3.10 <https://github.com/scrapy/parsel/blob/eb4657934cddb8b44726cda7893852c925bcda3a/.readthedocs.yml#L6-L11>`_.
- `Thebe`_, a Jupyter-powered tool to make HTML pages interactive,
  `needs Node.js to build the latest version of the code <https://github.com/executablebooks/thebe/pull/472>`_.

Do you think this feature will be useful for you as well?
Give it a try and let us know.

.. _cryptography: https://cryptography.io/
.. _parsel: https://parsel.readthedocs.io/
.. _Thebe: https://thebe.readthedocs.io/

Remember you can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_.

---

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!
