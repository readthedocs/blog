.. post:: Nov 10, 2022
   :tags: announcement, feature, builds
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      We released a new config key (``build.commands``) to specify user-defined commands
      which allows users to override the build process completely.


Override the build process completely with ``build.commands``
=============================================================

We are happy to announce a new *beta* feature that allows users to **override the Read the Docs build process completely**.
We previously talked about `executing custom commands <https://blog.readthedocs.com/user-defined-build-jobs/>`_ *in-between* the Read the Docs build process.
That approach is not sufficient for projects with a heavily customized build process,
or those that want to use a different documentation tool like Pelican_, Docsify_ and Docusaurus_ for their documentation.
Some of which were not able to use our platform at all.
Until now! We have good news for them!

.. _Pelican: https://getpelican.com/
.. _Docsify: https://docsify.js.org/
.. _Docusaurus: https://docusaurus.io/

The new configuration file option ``build.commands`` allows projects to only execute *exactly* the commands they want.
No more. No less.
This means that Read the Docs *won't execute any of the default commands* behind the scenes.
You have 100% control over the build process.


How does it work?
-----------------

To use the new *beta* feature,
you can specify all the commands the build process requires under the ``build.commands`` `config key <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-commands>`_.
Finally, move the resulting documentation artifacts into the ``_readthedocs/html`` directory.
Read the Docs will upload and host all the content of that folder ✨

Here is simple example that builds the Docusaurus tutorial:

.. code:: yaml

   version: 2

   build:
     os: ubuntu-22.04
     tools:
       nodejs: "18"
     commands:
       # "docs/" directory was created using the command to create the site:
       # npx create-docusaurus@latest docs classic
       #
       # Install Docusaurus dependencies
       - cd docs/ && npm install
       # Build the site
       - cd docs/ && npm run build
       # Copy generated files into Read the Docs directory
       - mkdir --parents _readthedocs/html/
       - cp --recursive docs/build/* _readthedocs/html/


The resulting documentation lives at https://test-builds.readthedocs.io/en/docusaurus/.

If you want to read more about ``build.commands``,
`read the full documentation <https://docs.readthedocs.io/en/latest/build-customization.html>`_.


Limitations
-----------

This feature is still in *beta* and has some limitation currently.
We are working to make ``build.commands`` more integrated into our platform.
One major missing feature is the flyout, which gives access to downloads, versions and other functionality.
We are actively working on improving this feature,
and we will publishing more content about this in the next months.
Stay tuned!


Try it out and give us feedback!
--------------------------------

We want to continue improving this *beta* feature.
It has lot of potential and we want to develop it in a way that's useful for our users.
Please, give it a try and `let us know <mailto:support@readthedocs.com>`_ how are you using it and if it's missing something for your use case.
