.. post:: August 2, 2023
   :tags: builders, deprecation
   :author: Manuel
   :location: BCN
   :category: Changelog

Sphinx default version installed is changed from 1.x to "latest"
================================================================

We are announcing the deprecation of building with Sphinx 1.x without specifying it in the project's dependencies.

Read the Docs **will stop installing Sphinx 1.x by default on projects**
that are not specifying that Sphinx version on their ``requirements.txt`` file.
We plan to deploy these changes on **October 3rd 2023**.
Make sure to perform the following changes before that date to avoid potentially unexpected failing builds.

Here you have a pretty simple example of the section required on the ``.readthedocs.yaml`` configuration file:

.. code-block:: yaml

   # ... snip ...

   python:
     install:
       - requirements: docs/requirements.txt

   # ... snip ...

The content of ``docs/requirements.txt`` would be similar to::

  sphinx==7.1.0

Read more about this in our `Reproducible builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`_ guide for more details.
