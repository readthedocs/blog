.. post:: August 2, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Drop support for MkDocs 0.17.3
==============================

Historically, Read the Docs has installed MkDocs ``0.17.3`` by default if the project didn't define a specific version of it.
Now, this version is a pretty old and we recommend our users to use the latest version of MkDocs. Currently, ``1.5.1``.

To avoid failing builds of projects using the version installed by default if we upgrade to the latest MkDocs version available,
we kept installing the old one during all this time.
Now, *we are changing that behavior to always install the latest available version* and we wanted to let you know about that so you can prepare your project.

**Starting on September 5th Read the Docs will install the latest available version of MkDocs**.
If you want to use a different version, make sure you are pinning your MkDocs dependency.

Here you have a pretty simple example of the section required on the `.readthedocs.yaml` configuration file:

.. code-block:: yaml

   # ... snip ...

   python:
     install:
       - requirements: docs/requirements.txt

   # ... snip ...

The content of `docs/requirements.txt` would be similar to::

  mkdocs==1.5.1

Read more about this in our `Reproducible builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`_ guide for more details.
