.. post:: Oct 12, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - October 2022
=========================================

September was exciting because a few members of our team finally got to gather in person.
Manuel, Benjamin, and Eric all attended Djangocon Europe in September,
and had lots of great discussions around documentation.

Also, as we mentioned, in Q4 we're going to be focusing on our core platform features.
This means we'll have fewer new features to talk about, 
but lots of smaller improvements to the overall experience of using Read the Docs.

New features
------------

The latest updates from our team:

- We fully rolled out support for auto-cancelling running builds when a user does multiple pushes to a branch in a small window of time. We wrote up a `full post <https://blog.readthedocs.com/cancel-old-builds/>`_ on the blog about it, where you can read more.
- Redirects can now be edited directly in our dashboard. This was an oversight that we are glad to have finally fixed the UX around.
- We fixed the bug we had previously mentioned around Gitlab tokens expiring. This caused PR builds for these users to stop properly reporting status. If you login with Gitlab again on our service, they will continue working indefinitely now.

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

Upcoming features
-----------------

Our roadmap hasn't progressed too much from last month,
and we continue to focus on these core platform upgrades:

- We're working on improving our integration with Material for MkDocs, which is a great theme for MkDocs documentation projects.
- Many improvements to our URL handling code, which will allow us to support more flexible URL configurations for projects.
- A search redesign to make it nicer across our dashboard and in-doc search experiences. 

Possible issues
---------------

We continue planning to be more active in deprecating old and outdated approaches to using our platform in Q4.
We don't have anything firm to announce here yet,
but we do plan to be more active in removing these features in the coming months.

We continue to actively deprecate jQuery from our code, as well as `guide the Sphinx ecosystem <https://github.com/sphinx-doc/sphinx/issues/10608>`_ through the transition. 

Tip of the month
----------------

This month's tip comes from our Twitter account:

.. raw:: html
   
   <blockquote class="twitter-tweet"><p lang="en" dir="ltr">Are you in doubt about which Sphinx theme to use? 🎨<br><br>Take a look at <a href="https://t.co/9w3JvCmlJj">https://t.co/9w3JvCmlJj</a> -- it has awesome live demos that will help you decide which theme is the best fit for your project. <a href="https://t.co/Hr1K2bbJhd">pic.twitter.com/Hr1K2bbJhd</a></p>&mdash; Read the Docs (@readthedocs) <a href="https://twitter.com/readthedocs/status/1570744372387540994?ref_src=twsrc%5Etfw">September 16, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
