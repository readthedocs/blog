.. post:: August 31, 2023
   :tags: addons, builders
   :author: Manuel
   :location: BCN
   :category: Feature announcement

New flyout re-desing in beta
============================

We are happy to announce the **beta release of a completely new flyout** that was re-written and re-designed from scratch.

After lot of hard work, we are happy to start rolling out the work of the new flyout to some projects.
Judging by its style, there are not big differences since it looks pretty close to the current one.
The main visual difference is that it now shows a Read the Docs logo when it's collapsed and expanded.


.. list-table::

   * - .. image:: img/new-flyout-collapsed.png
            :width: 85%
            :align: center
     - .. image:: img/new-flyout-expanded.png
            :width: 85%
            :align: center

However, taking into account the technical specifications, *everything has changed*.
There is no need to jump pretty deep into its details, but there are two main points we want to highlight here:

JS file is injected at serve time
    Previously, we were injecting CSS/JS files at build time by using a custom Sphinx extension (``readthedocs-sphinx-ext``) that we installed on behalf of the user when building on Read the Docs.
    On the other hand, for MkDocs projects, we were manipulating the ``mkdocs.yml`` file to add these files.

    Now, we are injecting *only one* self-contained JS file called ``readthedocs-addons.js`` at serving time via Cloudflare.
    This allows us to support any documentation tool (e.g. Docusaurus, Docsify, etc) without having to create a specific integration with it,
    helping with our goal of making our platform documentation tool agnostic.

The flyout is fully rendered based on a JSON API call
    The old implementation of the flyout does an API call that returns a blob HTML that our Javascript file injects directly on the page.
    This technique has a lot of limitations for theme authors since they cannot easily customize the flyout as they need.

    The new flyout is using a JSON API call that returns all the required data needed to render the flyout via Javascript.
    We plan to expose this JSON data via a Javascript event so theme authors can customize the flyout as they want,
    changing the style, positioning, or even the HTML structure of it.


All this work has been done under the umbrella of a new project that we called **"Read the Docs Addons"** (`repository <https://github.com/readthedocs/addons>`_),
where we plan to add multiple "reader features" in the near future.
These features include:

- Analytics
- Non latest version warning banner
- PR warning banner
- Search as you type
- Sponsorship via EthicalAds
- Visual documentation diff


As this work is still in beta, we haven't rolled it out to all the projects yet.
We have decided to start with projects using ``build.commands`` config key (`read more <https://docs.readthedocs.io/en/latest/build-customization.html>`_)
since those projects has no integrations at all with Read the Docs currently and they were missing a lot of good features.
Now, with the injection of the addons, those projects will start having most of the same integrations gradually until we reached parity with the old implementation.

`Let us know <mailto:support@readthedocs.org>`_ if you are using ``build.commands`` in your project and you have some feedback to share with us.
Also, if you find any issue with it, `report it in our issue tracker <https://github.com/readthedocs/addons/issues>`_ 😉
