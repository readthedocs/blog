.. post:: February 20, 2019
   :tags: feature
   :author: Santos
   :location: CUE

New Configuration File
======================

We are happy to announce the new version of the `Read the Docs configuration file`_ (v2).

.. _Read the Docs configuration file: https://docs.readthedocs.org/en/latest/config-file/v2

.. code-block:: yaml

   version: 2
   python:
     version: 3.7
     install:
       - requirements: docs/requirements.txt
   sphinx:
     configuration: docs/conf.py
   formats: all

If you are a recurrent Read the Docs user,
chances are that you've configured your projects using a `.readthedocs.yml` file.

Using the web interface is quick,
but the main advantages of using a configuration file over the web interface are:

- Some settings are only available using a configuration file.
  We are moving away from using the web interface.

- The settings are per version rather than per project.
  This would allow different versions of docs to be built with different versions of Python
  or different requirements.

- The settings live in your VCS.

- Reproducible build environments over time.

What did we change in the new version?
--------------------------------------

**All the configurations from the web interface**.
In the past not all options from the web interface were available in the configuration file,
now they are!
We also reorganized and renamed some options to make them more clear.

**New defaults**,
we don't merge the values from the web interface,
because this was confusing our users.
This also allows us to change defaults without breaking existing projects.

**More flexible installations**,
users can install their projects in a more flexible way,
like multiple requirements and packages from different locations.

**Strict validation** for invalid options in the configuration file,
to avoid typos and provide more feedback on invalid configurations.

New features
------------

- MkDocs support (previously it was only supported from the web interface).

.. code-block:: yaml

   version: 2
   mkdocs:
     configuration: mkdocs.yml
     fail_on_warning: true

- More control over Sphinx.

.. code-block:: yaml

   version: 2
   sphinx:
      builder: html
      configuration: docs/source/conf.py
      fail_on_warning: true

- Control over submodules, we don't always need them all to build our docs.

.. code-block:: yaml

   version: 2
   submodules:
     include:
       - third-party/dependency
     recursive: true

- Support for multiple packages/requirements installations.

.. code-block:: yaml

   version: 2
   python:
     version: 3.7
     install:
       - requirements: docs/requirements.txt
       - requirements: requirements.txt
       - method: pip
         path: package

Future improvements
-------------------

We are already planning new features to support more projects and use cases.

**Pipfile support**, this is one of our more requested features,
and we are going to ship it soon.
Keep an eye in `#3181`_.

**Show the configuration used in each build**.
We want to make more explicit to the users how we are building their docs.

**Redirects per version** of your docs.
Currently users can define global redirects only from the web interface,
this is hard to maintain and review.
One use case is when you change your docs structure between versions.
Keep track of this upcoming feature in `#4221`_.

.. _#3181: https://github.com/rtfd/readthedocs.org/issues/3181
.. _#4221: https://github.com/rtfd/readthedocs.org/issues/4221

Start using it
--------------

The full docs about the new version are available `here <http://docs.readthedocs.org/en/latest/config-file/v2>`__.

If you are using the v1, you can update to v2 following our `migration docs`_.

.. _migration docs: http://docs.readthedocs.org/en/latest/config-file/v2#migrating-from-v1

If you have a problem using the configuration file, feel free to `file an issue`_.

.. _`file an issue`: http://github.com/rtfd/readthedocs.org/issues

Summer internship
-----------------

This project was part of my summer internship in Read the Docs,
it was held at the same time as the Google Summer of Code (GSoC) project.

Thanks to the `core team`_ (Anthony, David, Eric, and Manuel) for helping me in the process.
Thanks to all contributors, sponsors, donors and users of Read the Docs to make the project sustainable.

.. _core team: https://docs.readthedocs.io/en/latest/team.html#development-team
