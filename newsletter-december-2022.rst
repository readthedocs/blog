.. post:: Dec 1, 2022
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - December 2022
========================================

Here are the first features and updates that have hatched since we announced a Q4 focus on core platform features in the :doc:`previous newsletter </newsletter-december-2022>`.


New features
------------

The latest updates from our team:

- Follow us in the Fediverse (Mastodon): `@readthedocs@fosstodon.org <https://fosstodon.org/@readthedocs>`_
- The *entire* build process can now be overridden (if you need it). :doc:`See the Announcement </build-customization>`
  - ...this is nice if you want to use a framework that isn't directly supported. We wrote some examples :ref:`Pelican <readthedocs:build-customization:pelican>` and :ref:`Docsify <readthedocs:build-customization:Docsify>`.
  - ...but you can also *extend* the build process for instance you can :ref:`skip a build <readthedocs:build-customization:cancel-build-based-on-a-condition>`!
- We are getting ready for Sphinx 6, almost there! (scroll down for details)
- :doc:`Server-Side Search API v3 <readthedocs:server-side-search/index>` has been released.
- We organized a larger refactor of our user documentation to comply with the `Diátaxis methodology framework <https://diataxis.fr>`_. So far, we broke it down into `73 tasks and counting <https://github.com/readthedocs/readthedocs.org/issues?q=is%3Aissue++diataxis+iteration+>`_. The tasks are big and small.

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.


Upcoming features
-----------------

(from last newsletter)

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


.. _december2022_tip_of_the_month

Tip of the month
----------------

TBD

Awesome Project of the month
----------------------------

TBD

Awesome Read the Docs Projects List 🕶️
--------------------------------------

Looking for more inspiration? Check out our new list: `Awesome Read the Docs Projects <https://github.com/readthedocs-examples/awesome-read-the-docs>`_.

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
