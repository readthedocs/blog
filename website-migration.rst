.. post:: Mar 3, 2023
   :tags: website, migration 
   :category: Changelog

.. Categories: https://docs.google.com/document/d/1io3HN61wpFtb6XP-cyONhV5CNWiZ5dbhZM4nvifyT5g/edit#heading=h.3xtrxdnntzqi

Read the Docs website migration to about.readthedocs.com
========================================================

Read the Docs is in the process of migrating our primary marketing website to a single site: https://about.readthedocs.com.
The new site offers users more information about our products and their features,
in a combined presentation of what was previously divided between two websites (Read the Docs Community and Read the Docs for Business).
At the same time, the new site will also serve as a single entrypoint for users that are logging in to Read the Docs accounts.
There has been a good deal of confusion around our two sites,
and this change makes it more clear which site you're going to.

Importantly,
**we are keeping both our Community and Business sites separate for logged in users.**
There are no changes in our commitment to offering free hosting for open source,
or the separation of infrastructure for Business customers.

.. figure:: /img/screenshot-new-website.png
    :alt: A screenshot of our beautiful new website

    Our beautiful new website, ready for our users!

Marketing website migration process
-----------------------------------

The process that we're taking to migrate our marketing site is as follows:

#. ✅ The initial work here was creating a proper marketing site,
   and deploying it to https://about.readthedocs.com.
   This was done in January 2023.
#. ✅ Redirecting *logged out* Business (``readthedocs.com``) users to the new site.
   This was done in February 2023, and we've been monitoring the impact of this change.
#. The final step will be to redirect *logged out* Community (``readthedocs.org``) users to the new site.
   This will happen in Q2 2023,
   as we want to make sure the experience is smooth for users who are used to browsing our current site.

We're excited about our new website,
because historically we have done a poor job of explaining our products.
Being able to have a single site that explains the features of our various sites,
and the value that Read the Docs brings to the documentation ecosystem is exciting for us.

Technical details
-----------------

Historically,
our marketing pages were generated from our Django application,
and updated only when we deployed a new version of the site.
With our new approach,
our marketing site is actually hosted by Read the Docs itself.

Self-hosting our marketing website gives us many benefits that our users love about hosting their docs with us:

* A proper static site generator built for making a website and blog.
* Pull request previews to allow us to review content changes.
* Instant deployment of updates whenever we merge to ``main``.
* All the rest of our :doc:`readthedocs:reference/features` that we offer to our users.

We're using our new :doc:`readthedocs:build-customization` feature to build our site with `Pelican <https://getpelican.com/>`__,
and it's been a really fun way to expand the capabilities of our build system.

We hope that you'll join us for the next stage of Read the Docs,
where we will continue to provide the best documentation hosting for all software projects.
