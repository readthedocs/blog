.. post:: Jun 5, 2023
   :tags: builders, deprecation
   :author: Manuel
   :location: BCN
   :category: Changelog

Remove support for Sphinx 1.x
=============================

We are announcing the deprecation of building with Sphinx 1.x without specifying it in the project's dependencies (``requirements.txt``).

Read the Docs **will stop installing Sphinx 1.x by default on projects created before October 20, 2020**
that are not specifying a Sphinx version on their ``requirements.txt`` file.
We plan to deploy these changes on **September 2023**.
Make sure to perform the following changes before that date to avoid potentially unexpected failing builds.

The main reason behind this decision is that users with old projects that create a new one are confused about the different Sphinx version installed.
On new projects Read the Docs installs the latest Sphinx version available (currently, 7.x),
while on projects created before October 20, 2020 installs Sphinx 1.x.
Besides, Sphinx 1.x has been unsupported for a long time now,
and `we've experiencend some breaking changes when there are new releases of its dependencies <https://github.com/readthedocs/readthedocs.org/issues/9037>`_.


Adding a ``requirements.txt``
-----------------------------

If you have a project on Read the Docs that is not using a ``requirements.txt`` to pin the Sphinx version,
**we strongly recommend you to create one as soon as possible** to avoid breaking builds once we deploy the changes.

Here you have a minimal ``requirements.txt`` file that you can copy and paste to use in your project.
With this config file your project should build successfully now
and will keep working fine once we deploy the changes in September 2023.

.. code::

   # docs/requirements.txt
   sphinx==6.2.1


Once you have created this file,
you have to tell Read the Docs to install these depedencies.
This is done by using the ``python.install.requirements`` key in the ``.readthedocs.yaml`` configuration file
as shown in the following example:

.. code:: yaml

   # ... your other configurations

   python:
     install:
       - requirements: docs/requirements.txt


.. note::

   If you don't have a ``.readthedocs.yaml`` configuration file already in your repository,
   you should create one first.
   Read more about it in our
   `documentation <https://docs.readthedocs.io/en/stable/config-file/v2.html>`_


Once you added the ``requirements.txt`` file and made the required changes in the ``.readtehdocs.yaml`` file,
you are ready to trigger a new build and double-check that it worked as expected.


Contact us
----------

Get in touch with us `via our support`_
and let us know if you any trouble pining your Sphinx dependency.

.. _via our support: https://readthedocs.org/support/
