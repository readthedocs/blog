.. post:: May 5, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features from May.

Read the Docs newsletter - May 2021
===================================

Welcome to a new edition of our monthly newsletter, where we
openly share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

-  We reworked our deploy procedure to almost remove the need to interrupt builds.
   Therefore, you should see less build retries during our deploy timeframe.
-  After some careful deliberation,
   we started the process to `deprecate recommonmark in favor of
   MyST <https://github.com/readthedocs/recommonmark/issues/221>`_,
   a better maintained alternative.
   We are excited to see that
   some projects have already migrated without effort,
   and we are looking forward to helping MyST-Parser thrive!
   Thanks to the Executable Books Project folks for creating this project.

.. Pageviews stats obtained from Google Analytics, https://readthedocs.io property,
   and divided by the total number of days in the month

New features
------------

-  We improved several areas of our contributor documentation:
   `we added more detailed steps on how to contribute to our
   docs <https://docs.readthedocs.io/en/stable/development/docs.html>`_
   (both from the GitHub UI and from your own computer),
   and we expanded our `development installation
   guide <https://docs.readthedocs.io/en/stable/development/install.html>`_
   with more clear instructions for static assets
   and some extra verification procedures.
-  We rolled up `a new keyword detection algorithm in our ad
   client <https://github.com/readthedocs/ethical-ad-client/pull/48>`_,
   which should make the ads you see more meaningful and useful.

You can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_ and `Ethical Ad Server
Changelog <https://ethical-ad-server.readthedocs.io/page/developer/changelog.html>`_.

Current focus & known issues
----------------------------

-  We are working with the Sphinx maintainers
   to help testing the upcoming Sphinx release
   and decrease the risk of breakage.
   It is an ongoing effort that requires
   finding a balance between stability and maintainability,
   and we hope we can do the best for our users and the Sphinx community.
-  xxx

Upcoming features
-----------------

-  xxx

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Anthony: https://github.com/agjohnson
.. _David: https://github.com/davidfischer
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
