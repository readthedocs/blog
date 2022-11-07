.. post:: Nov 7, 2022
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - November 2022
========================================

Here are the first features and updates that have hatched since we announced a Q4 focus on core platform features in the :doc:`previous newsletter </newsletter-october-2022>`.


New features
------------

The latest updates from our team:

- :doc:`sphinx-rtd-theme 1.1.0 </theme-release-110>` has been released with minor improvements and as a big step towards future releases with larger changes.
- After rolling out auto-cancelling builds `last month <https://blog.readthedocs.com/cancel-old-builds/>`_, we have already recorded a whopping 10% decrease in builds.
  We're really happy with how this turned out, not least that it effectively reduces our cloud footprint by 10% 🌱.
- We started incrementally refactoring our own documentation to match the `Diátaxis framework <https://diataxis.fr/>`_. We will be writing more about this, as we are currently gaining practical experience.
- Much thanks to `AA-Turner <https://github.com/AA-Turner>`_ and the Sphinx community for working together on a proposal and releasing the extension `sphinxcontrib-jquery <http://pypi.org/project/sphinxcontrib-jquery>`_. This extension is required for themes and extensions that need jQuery from Sphinx 6 and onewards. Sphinx 6.0 is scheduled for December 2022 and will no longer bundle jQuery.

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.


Upcoming features
-----------------

- A 1.2.0 release of :ref:`sphinx-rtd-theme <sphinx_rtd_theme110_upcoming_releases>` will support docutils 0.18 and Sphinx 6.
- We're working on improving our integration with Material for MkDocs, which is a great theme for MkDocs documentation projects.
- Many improvements to our URL handling code, which will allow us to support more flexible URL configurations for projects.
- A search redesign to make it nicer across our dashboard and in-doc search experiences. 
- 404 pages are being improved by contextualization the user message, giving relevant guidance to readers and project owners.


Possible issues
---------------

If you find regressions in any new releases of the `sphinx-rtd-theme <https://sphinx-rtd-theme.readthedocs.io/>`_,
please don't hesitate to `open an issue on GitHub <https://github.com/readthedocs/sphinx_rtd_theme/>`_.

We continue planning to be more active in deprecating old and outdated approaches to using our platform in Q4.
We don't have anything firm to announce here yet,
but we do plan to be more active in removing these features in the coming months.


.. _november2022_tip_of_the_month

Tip of the month
----------------

This tip of the month comes from our own experience. We have greatly benefitted from the following two Python/Django projects:

- `blacken-docs <https://github.com/adamchainz/blacken-docs>`_ is a pre-commit linter that checks and formats your Python code embedded in your documentation. In other words, it helps you make sure that your documentation's code examples look great.
- `django-upgrade <https://github.com/adamchainz/django-upgrade>`_ saves us a lot of time each time we upgrade to the latest Django version.

As you might have noticed, both of these projects are maintained by `Adam Johnson <https://adamj.eu/>`_. Thanks, Adam 👋


Awesome Project of the month
----------------------------

`As we also tweeted <https://twitter.com/readthedocs/status/1581949857865965569>`_, we are really big fans of how the `Wagtail <https://wagtail.org/>`_ community has built its documentation on `docs.wagtail.org <https://docs.wagtail.org/>`_. Our favorite parts are...

Custom theme 🎨:
  Wagtail uses a beautiful custom Sphinx theme with dark mode support

Release notes 🚢:
  Its documentation includes carefully curated 💅​ release notes that developers are happy to read. They include what’s new, bug fixes, new features and upgrade notes between versions. Take a look at their `latest major release notes <https://docs.wagtail.org/en/latest/releases/4.0.html>`_.

Contribution guide 👩‍👩‍👧​👨‍👨‍👦‍👦​:
  Wondering how to write a GOOD “Contribution guide” 👩‍👩‍👧​👨‍👨‍👦‍👦​👨‍👩‍👧‍👦​​? Take a look at Wagtail's `Contribution Guide <https://docs.wagtail.org/en/latest/contributing/index.html>`_. It gives a brief overview of how you can contribute and once you have decided what you want to do, you can read more in 11 carefully crafted categories.

Personas 👩🏽‍💻​:
  Wagtail divides the readers in two categories: “developers 👩🏽‍💻​ that want to install and maintain their Wagtail instance” and “users👨‍💼 of a Wagtail-powered site”. This makes it easier for each of these two personas to find what they are looking for immediately.

5 out of 6 contributors write documentation 🎉 🎉 🎉:
  Wagtail has a stunning amount of documentation contributors! Out of the ~600 contributors to Wagtail, ~500 of those have written documentation. Most of them added changelog entries or release notes, since adding code changes requires updating the changelog. This is a great way to potentially turn your code contributors into documentation contributors.

Awesome Read the Docs Projects List 🕶️
--------------------------------------

Looking for more inspiration? Check out our new list: `Awesome Read the Docs Projects <https://github.com/readthedocs-examples/awesome-read-the-docs>`_.

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
