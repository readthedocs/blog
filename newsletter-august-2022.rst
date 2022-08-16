.. post:: Aug 17, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - August 2022
======================================

We continue to be excited about the expanded capacity we have with an additional team member.
Our focus for July has been around a lot of marketing and positioning, 
trying to better understand how our customers view our product,
and work with them to use it well.

We also had our `12th birthday <https://twitter.com/readthedocs/status/1559575996558221312>`_ just before publishing this newsletter. 🎉

New features
------------

We've continued building a number of features and bug fixes in our roadmap:

- We have more **Example projects**, which allow users to `get started quickly`_ with our products. We shipped an example for JupyterBook this month, which is of growing interest to our scientific users.
- Scientific users are important for us, so we've put together a `landing page <https://docs.readthedocs.io/en/latest/science.html>`_ that highlights the benefits that our scientific users are seeing. 
- We created a `GitHub action <https://github.com/readthedocs/actions>`_ that allows users to have a link to the Pull Request preview automatically added to the PR description. If users find this useful, we will continue to expand this functionality, and perhaps add it to our core platform so no configuration is needed. 
- We improved the security and safety of our platform by making sure all invites for a team or project have to be approved by the user.


You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

.. _get started quickly: https://docs.readthedocs.io/en/latest/examples.html
.. _flyout menu: https://docs.readthedocs.io/en/latest/flyout-menu.html

Awesome documentation projects
------------------------------

We are collecting entries for `Awesome Read the Docs Projects`_ - please do tell us about your favorites, either by sending an email or `opening a Pull Request`_!

-  `Weblate <https://docs.weblate.org/en/latest/>`__ - Weblate is a
   translation platform with a large documentation project with many
   translations and customized Read the Docs theme. Documentation aimed
   at all segments: users, administrators and developers. Also features
   an extensive Changelog. 
-  `TomoBank <https://tomobank.readthedocs.io/>`__ - a big list of
   tomographic datasets and phantoms, featuring especially tables and
   images and maintained by science community.
-  `Uberspace <https://manual.uberspace.de/>`__ - Customized sidebar and
   footer, adding project's branding through custom CSS and HTML to
   ``sphinx_rtd_theme``. Latest version and release date on front page.

.. _Awesome Read the Docs Projects: https://github.com/readthedocs-examples/.github/
.. _opening a Pull Request: https://github.com/readthedocs-examples/.github/blob/main/contributing.md

Upcoming features
-----------------

- We are working on some improvements to our URL handling code, which will allow us to support more flexible URL configurations for projects.
- As mentioned before, we are shifting some of our focus to frontend & marketing these next few months. We're getting close to shipping our new landing page, which we're excited about.
- We're continuing to focus on outreach for our new build customization features, so that we can continue to improve them with your feedback.

Possible issues
---------------

We are actively working to deprecate jQuery from our code, as well as `guide the Sphinx ecosystem <https://github.com/sphinx-doc/sphinx/issues/10608>`_ through the transition. 

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
