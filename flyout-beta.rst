.. post:: August 31, 2023
   :tags: addons, builders
   :author: Manuel
   :location: BCN
   :category: Feature announcement

Documentation Addons beta
=========================

After lot of hard work, we are happy to announce that our new project,
`Read the Docs Addons`_, is ready for beta testing.

What are Addons?
----------------

`Addons`_ is a new project that aims to bring all of our features to new
documentation tools and replace features that currently only support Sphinx
or MkDocs. The most prominent feature the you will notice from this project is
our flyout menu.

.. list-table::

   * - .. image:: img/new-flyout-collapsed.png
            :width: 85%
            :align: center
     - .. image:: img/new-flyout-expanded.png
            :width: 85%
            :align: center

We redesigned everything from the ground up in order to address limitations of our current features:

Supporting new documentaiton tools is difficult
    Right now, we only support Sphinx and MkDocs and are injecting our hosting features at build time using custom extensions for each tool.
    In order to support new documentation tools,
    we must maintain a new extension for each tool we want to support.

Features aren't supported by all documentation tools
    Maintaining multiple extensions has also lead to differences in the features each tool supports,
    as we have to rely on the integrations available in each tool.

Customization is difficult
    We also can not offer easy customization of features like our flyout menu due how they are injected into hosted documentation. 

The documentation features that Addons currently supports are:

- Our flyout menu
- Analytics
- Non-latest version warning banner
- Pull request warning banner
- Search as you type
- Sponsorship via EthicalAds

Eventually, all documentation tools will use this same library, including Sphinx
and MkDocs, and all tools will have the same access to our documentation
features.

How to use Addons
-----------------

We decided to limit beta testing to projects using the ``build.commands`` configuration key [1]_.
These projects did not have any of our documentation features,
like our flyout menu or search,
as our documentation tool extensions do not execute for these projects.
If you are using this configuration option already,
your project is already using the new Addons library.

.. TODO is there a way users can opt out of this beta without contacting us?

If you would like to opt out of the beta, `contact us <mailto:support@readthedocs.org>`_.

What has changed
----------------
          
On the technical implementation, *everything has changed*.
This is a full rewrite of these features so there is a lot to mention here,
but there are two main points to highlight:

JavaScript is injected while serving documentation 
    Instead of injecting our features while building documentation,
    we are injecting *only one* self-contained JavaScript file,
    called ``readthedocs-addons.js``, at serving time via Cloudflare Workers.
    This allows us to support any documentation tool (e.g. Docusaurus, Pelican, Docsify, etc) without having to create a specific extensions for it.
    This helps with our goal of making our platform documentation tool agnostic.

The flyout is rendered using a JSON API call
    Our current flyout menu is rendered by the application and injected by the client as a chunk of HTML.
    This approach is difficult to customize and style however.
    Instead, the new flyout is rendered using a JSON API call that returns all the required data needed to render the flyout via JavaScript.
    We plan to expose this JSON data via a JavaScript event so theme authors can customize the flyout as they want,
    changing the style, positioning, or even the HTML structure.

`Let us know <mailto:support@readthedocs.org>`_ if you are using ``build.commands`` in your project and you have some feedback to share with us.
Also, if you find any issue with it, `report it in our issue tracker <https://github.com/readthedocs/addons/issues>`_ 😉

.. [1] You can read more on build customization and how to use ``build.commands`` to control the entire build process here: https://docs.readthedocs.io/en/latest/build-customization.html

.. _Addons: https://github.com/readthedocs/addons
.. _Read the Docs Addons: https://github.com/readthedocs/addons
