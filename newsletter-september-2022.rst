.. post:: Sep 9, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - September 2022
=========================================

Our focus for August has continued to be around marketing and community outreach.
We continue to better understand how our customers view our product,
and work with them to use it well.

We're working to establish our goals for Q4 2022,
and it looks like continued focus on polishing core platform features.
We have a *lot* of features,
and we need to continue making them easier to use.

New features
------------

The latest updates from our team:

- 🎉 We have soft launched the `initial version of our new landing pages <https://about.readthedocs.com/>`_ and started sharing it with the community. We plan to eventually have this as our primary landing page once we've gotten more feedback on it. 
- We have improved out logic for `cancelling builds when a commit is pushed to an already building version <https://github.com/readthedocs/readthedocs.org/pull/9549>`_. This will improve user experience waiting on a build that will be overwritten, and save our servers some time as well!
- We continued improving our docs pages. This month we did `badges <https://github.com/readthedocs/readthedocs.org/pull/9580>` & `build troubleshooting <https://docs.readthedocs.io/en/stable/build-troubleshooting.html>`_.
- A lot of work has continued to standardize our codebase on the ``djstripe`` package, instead of our own custom stripe webhook implementation.
- We improved our custom domain handling so that users who haven't properly activated their domain will get reminded about it a few times, and then we'll stop trying to configure it.

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

Upcoming features
-----------------

- We continue to work on improvements to our URL handling code, which will allow us to support more flexible URL configurations for projects.
- We are working to redesign some of our search to make it nicer across our dashboard and in-doc search experiences. 
- Our telemetry data is starting to really come together, and we're gathering insights on interesting metrics around builds. Expect a few blog posts about this in the coming months.
- The 1.1 release of our `sphinx_rtd_theme` had a large amount of work done, and is nearing release.

Possible issues
---------------

We are planning to be more active in deprecating old and outdated approaches to using our platform in Q4.
We don't have anything firm to announce here yet,
but we do plan to be more active in removing these features in the coming months.

We continue to actively deprecate jQuery from our code, as well as `guide the Sphinx ecosystem <https://github.com/sphinx-doc/sphinx/issues/10608>`_ through the transition. 

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
