.. post:: March 30, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - April 2023
=====================================

News and updates
----------------

- 📚️ We refactored our user documentation to align with the `Diátaxis Framework <https://diataxis.fr>`__ and now the navigation sidebar and the landing page are so much better! 
  Have a look at `docs.readthedocs.io <https://docs.readthedocs.io/en/stable/>`__.
- 🌄️ The first proof-of-concept for a new API and JavaScript library is running and capable of displaying a menu matching our current :doc:`flyout menu <readthedocs:flyout-menu>`.
  The big difference will be that the new API and library will be useful for any documentation framework or static site generator to allow for full control of the new flyout menu and access to API data.
- ⚙️ Added a new build variable ``READTHEDOCS_CANONICAL_URL`` that's useful for projects that want to be aware of the canonical base URL while building.
  `Read more in our docs <https://docs.readthedocs.io/en/stable/reference/environment-variables.html#envvar-READTHEDOCS_CANONICAL_URL>`__.
- 📊️ All of our websites now use `Plausible <https://plausible.io/>`__ for analytics.
- 🔒️ Fixed vulnerability: `Cache poisoning: serving arbitrary content on documentation sites  <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-mp38-vprc-7hf5>`__

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

.. figure:: img/screenshot-docs-diataxis-update.png
   :alt: A screenshot of our current documentation after the refactor
   
   Here is how our documentation looks in April 2023.


Upcoming features
-----------------

- 📚️ We are still doing changes in our documentation structure and content.
- ⚡️ *A lot of work* is happening these days on bigger features.
  In :doc:`the last newsletter </newsletter-march-2023>`, we mentioned the new Dashboard.
  On the side of that,
  we are also building a new generic JavaScript client and API that will give additional features to any documentation project or static site built on the platform.

.. figure:: img/screenshot-search-integration-docusaurus.png
   :alt: A screenshot of the upcoming search dialogue running on Docusaurus
   
   Our proof-of-concept is going well! In the screenshot, you can see how the generic Read the Docs search indexing works and how a generic search dialog gives the documentation project additional super powers ⚡️

Want to follow along with our development progress? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1


.. Possible issues
.. ---------------

.. - TBD


Awesome project of the month
----------------------------

`Crate.io <https://crate.io/docs/crate/tutorials/en/latest//>`__ has for over a decade gathered 15 Sphinx projects in the same website experience and written their own theme.
So they rightly deserve to be this month's addition to `Awesome Read the Docs Projects 🕶️ <https://github.com/readthedocs-examples/awesome-read-the-docs>`_.
See our chosen highlights from Stack's documentation in the following
`Twitter thread <https://twitter.com/readthedocs/status/1633101744312909827>`__ and
`Mastodon thread <https://twitter.com/readthedocs/status/1633101744312909827>`_:

.. raw:: html

   <blockquote class="twitter-tweet"><p lang="en" dir="ltr">The Haskell Tool Stack is a packaging tool for <a href="https://twitter.com/hashtag/haskell?src=hash&amp;ref_src=twsrc%5Etfw">#haskell</a>. Because their documentation is so awesome, it’s also their main website 💯<br><br>Stack’s website is maintained with GitHub, MkDocs, and Read the Docs: <a href="https://t.co/GaCTgxTUcm">https://t.co/GaCTgxTUcm</a><br><br>Here is a 🤏 (small) 🧵 about why it’s awesome 🕶️ <a href="https://t.co/wdAQ3NigHK">pic.twitter.com/wdAQ3NigHK</a></p>&mdash; Read the Docs (@readthedocs) <a href="https://twitter.com/readthedocs/status/1633101744312909827?ref_src=twsrc%5Etfw">March 7, 2023</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 


.. Tip of the month
.. ----------------

.. TBD

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
