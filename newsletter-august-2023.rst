.. post:: August 4, 2023
   :tags: newsletter, python
   :author: Eric
   :location: BND
   :category: Newsletter

Read the Docs newsletter - August 2023
======================================

News and updates
----------------

- 🏝️ A few team members took vacations this month, and everything kept running smoothly, which is always wonderful to see.
- 💵 We are working to simplify our subscriptions on |com_brand|, to make it easier for customers to know what they are getting, and for us to ensure all the features in each plan align with our pricing page.
- 🔒 We shipped a `change to authentication <https://github.com/readthedocs/readthedocs.org/pull/10498>`_ on our build servers to dramatically reduce the permissions required when building documentation.
  This increases our "defense in depth" security posture, and reduces the risk of a security breach.
- ⏰ Continuing deprecations:
  We have a number of old feature deprecations underway. 
  The goal here is to reduce complexity of our build platform,
  and enable users to control their own builds via ``build.tools`` and ``build.commands`` instead of feature flags.
  You can see the full list and timeline on `issue #10587 <https://github.com/readthedocs/readthedocs.org/issues/10587>`_.

You can always see the latest changes to our platforms in our `changelog <https://docs.readthedocs.io/page/changelog.html>`_.

Upcoming features
-----------------

- Our marketing website (https://about.readthedocs.com/) transition will be finishing up next week.
  We will be redirecting all logged out |org_brand| users to the new site, completing this migration.
- We continue to finish rolling out our updated Proxito v2 code. This is fully rolled out to |org_brand|,
  and has a couple customers we're waiting on to migrate |com_brand|. This will happen in August.
- We are rolling out HTML search indexing for all projects. This removes a small bit of functionality from our search for Sphinx projects,
  but makes it much more reliable across all documentation tools.
- We continue to work on a revamped flyout using our `addons <https://github.com/readthedocs/addons>`_ system.
  This is the first step in a larger project to improve the user experience of our documentation platform.

Want to follow along with our development progress? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1

Possible issues
---------------

- We continue to simplify our product by issuing deprecations.
  You can see the full list and timeline on `issue #10587 <https://github.com/readthedocs/readthedocs.org/issues/10587>`_,
  and make sure your're not affected by any of them.

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_ or just reply to this email.

.. _Contact us: mailto:hello@readthedocs.org

