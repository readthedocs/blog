.. post:: Nov 10, 2022
   :tags: announcement, feature, builds
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      We released a new config key (``build.commands``) to specify user-defined commands
      which allows users to overwrite the build process completely.


Overwrite the build process completely
======================================

We are happy to announce a new *beta* feature that allow users to **overwrite the build process completely**.
In the past, `we talked about executing custom commands <https://blog.readthedocs.com/user-defined-build-jobs/>`_ *in-between* the Read the Docs build process.
However, that approach may not be enough for some projects with strong custom build processes
and they were not able to use our platform because of that.
Until now! We have good news for them!

The new key ``build.commands`` allows projects to only execute *exactly* the commands they want.
No more. No less.
This means that Read the Docs *won't execute any of the default* commands behind the scenes.
You have 100% control over the building process.


How it works?
-------------

To use the new *beta* feature,
you can specify all the commands the build process requires under the ``build.commands`` `config key <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-commands>`_.
Finally, move the resulting documentation artifacts into the ``_readthedocs/html`` directory.
Read the Docs will upload and host all the content of that folder ✨

Here is simple example that builds a small project's documentation using `Docsify <https://docsify.js.org/>`_:

.. code:: yaml

   version: 2
   build:
     os: "ubuntu-22.04"
     tools:
       python: "3.11"
     commands:
       # Create the output directory
       - mkdir --parents _readthedocs/html/
       # Copy the documents (including the ``index.html``)
       # into the output directory
       - cp --recursive docs/* _readthedocs/html/

If you want to read more about ``build.commands``,
`read the full documentation <https://docs.readthedocs.io/en/latest/build-customization.html>`_.


Limitations
-----------

As we mentioned before,
this feature is still in *beta* and has some limitation currently.
We are working towarsd making ``build.commands`` more integrated into our platform features.
Mainly, the flyout with links to the Read the Docs project and all its active versions.
We are close to get there,
and we will publishing more content about this in the next months.
Stay tunned!


Try it out and give us feedback!
--------------------------------

We want to continue improving this *beta* feature.
It has lot of potential and we want to develop it in a way that's useful for our users.
Please, give it a try and `let us know <mailto:support@readthedocs.com>`_ how are you using it and if it's missing something for your use case.
