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


News and updates
----------------

The latest updates from our team:

- 🐘️ We started *tooting* in the Fediverse (Mastodon): `@readthedocs@fosstodon.org <https://fosstodon.org/@readthedocs>`_
- 🎬️ Visit the upcoming landing page `about.readthedocs.com <https://about.readthedocs.com/>`_ and let us know if you have comments or ideas for it.
- ⚙️ The *entire* build process can now be overridden (if you need it). :doc:`See the Announcement </build-customization>`.

  - 💡️ ...this is useful if you want to publish outputs generated from a framework that isn't supported by default. We wrote some examples for :ref:`Pelican <readthedocs:build-customization:Pelican>` and :ref:`Docsify <readthedocs:build-customization:Docsify>`.
  - 💡️ ...you can also *extend* the build process for instance you can :ref:`skip a build <readthedocs:build-customization:Cancel build based on a condition>`.

- ⬇️ Sphinx 6 is coming soon, more details :ref:`further down <sphinx6_is_coming>`.
- 🛳️ :doc:`Server-Side Search API v3 <readthedocs:server-side-search/index>` has been released.
- ⏳️ We organized a large refactor of our user documentation to comply with the `Diátaxis methodology framework <https://diataxis.fr>`_.
  So far, we broke it down into `73 tasks and counting <https://github.com/readthedocs/readthedocs.org/issues?q=is%3Aissue++diataxis+iteration+>`_.
  The tasks are big and small.
- ✅️ We added :doc:`readthedocs:unofficial-projects`.
- ✅️ We added `an additional auditing feature <https://github.com/readthedocs/readthedocs.org/pull/9607>`_,
  whereby invitations are added to the Security Log.
  The feature is available for users of Read the Docs for Business.
- ✅️ We found, fixed and disclosed a security issue,
  `XSS: Allow serving of arbitrary HTML files from main domain <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-98pf-gfh3-x3mp>`_.

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.


.. _sphinx6_is_coming:

Sphinx 6 is coming
------------------

Sphinx 6 is not yet released, but it may be released before the arrival of our next newsletter.
Here are some of our considerations for getting ready for Sphinx 6:

- Sphinx 6 focuses on reducing the maintenance burden for the future,
  dropping support of docutils 0.14, 0.15, 0.16 and 0.17.
  This will make the work of theme and extension maintainers considerably easier,
  and we may start seeing themes requiring ``Sphinx>=6`` simply because it's less work to support.
- Sphinx 6 requires docutils 0.18 or 0.19.
  We are finalizing support for `sphinx-rtd-theme`_ which currently only supports docutils 0.17.
  These updates are almost finished and are planned to arrive in sphinx-rtd-theme 1.2.0.
- Sphinx 6 is removing jQuery, but we need it for `sphinx-rtd-theme`_.
  jQuery is easily added back using the new extension `sphinxcontrib-jquery`_.
- Sphinx 6 removes all bundled JavaScript libraries.
  If you depend on any of these,
  you may have to bundle them yourself or modify your implementation.

Since most documentation projects rely on themes and extensions, we recommend that you do not upgrade to Sphinx 6 before you see announcements of Sphinx 6 support in your themes and extensions.

.. _sphinx-rtd-theme: https://sphinx-rtd-theme.readthedocs.io/
.. _sphinxcontrib-jquery: https://pypi.org/project/sphinxcontrib.jquery/


Upcoming features
-----------------

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


.. _december2022_tip_of_the_month:

Tip of the month
----------------

Do you need to document past or upcoming events? `Chris Sewell <https://github.com/chrisjsewell>`_ has created `sphinx-timeline <https://sphinx-timeline.readthedocs.io/en/latest/>`_ for exactly this.

See sphinx-timeline in full action on the `main page of AiiDA <https://www.aiida.net/>`_.

Awesome Project of the month
----------------------------

`Nautobot <https://docs.nautobot.com/>`_ is a great example of a documentation landing page with several subprojects. See `this Twitter thread <https://twitter.com/readthedocs/status/1595010133796462593>`_ for screenshots and comments.


Awesome Read the Docs Projects List 🕶️
--------------------------------------

Looking for more inspiration? Check out our new list: `Awesome Read the Docs Projects <https://github.com/readthedocs-examples/awesome-read-the-docs>`_.

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
