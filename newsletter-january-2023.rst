.. post:: Jan 1, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - January 2023
=======================================

Happy 2023!

News and updates
----------------

Here are the latest updates from our team since the :doc:`previous newsletter </newsletter-december-2022>`:

- 📹️ Eric delivered a talk at DjangoCon US 2022 with practical tips for developing *state of the art* documentation projects.
  You can watch it here: `Documenting Django Code in 2022`_
- 🛠️ In line with the talk,
  we continued reorganizing our own documentation to follow the `Diátaxis Framework`_.
- 🚢️ Sphinx 6.0 and 6.1 have been released.
  If you want things to not break,
  it's good to wait a bit.
  Read :doc:`our considerations for upgrading </sphinx6-upgrade>`.
- 🔒️ We fixed a security vulnerability on our platform. See: `GHSA-368m-86q9-m99w`_

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

.. _Documenting Django Code in 2022: https://www.youtube.com/watch?v=mqn0D4xat58
.. _Diátaxis Framework: https://diataxis.fr/
.. _GHSA-368m-86q9-m99w: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-368m-86q9-m99w

Upcoming features
-----------------

..
  Note:
  
  When creating newsletter drafts, we keep the items here from the previous newsletter.
  This is in order to ensure due follow-up on features that are announced publicly.
  
  Feature done? A great follow-up is to add what was previously an upcoming feature as a released feature in the former section.
  
  Feature not done?
  Make sure that upcoming features are announced with a link to issues or PRs where the progress can be seen.
  If this is done, then subsequent newsletters aren't compelled to share progress when it's uninteresting.
  
  If a feature was announced as upcoming but isn't yet released,
  then try rephrasing the announcement as a general news update about the progress and where it can be followed.

The core team has laid out its 2023 Q1 roadmap and our general focus will be on:

- Improving support for using *any* documentation tool in the build process.
- Currently, users can either customize a default build process or overwrite the entire process from scratch.
  We are aligning these two approaches,
  making it easier to design and configure builds for a project's individual needs.
- Continuing to restructure and rewrite the user documentation of Read the Docs.
  We look forward to publishing the restructured documentation which is likely happening at the end of Q1.
- Dashboard redesign: The entire Dashboard will be redesigned and re-implemented.
  This work is about to be launched!


Possible issues
---------------

Sphinx users should be aware that Sphinx 6.0 and 6.1 were released very recently.
If you haven't pinned dependencies,
the update might come automatically.
If you choose to update,
there are a few things to be aware of.
Read :doc:`our considerations for upgrading </sphinx6-upgrade>`.

..
  Tip of the month
  ----------------
  
  TBD: Insert twitter embed


Awesome Project of the month
----------------------------

`GeoPandas <https://geopandas.org/>`_ is an open source project for working with geospatial data which requires a lot of exciting features from the documentation - maps, plots etc. We especially like how the documentation is structured. See all the highlights in the following `Twitter thread <https://twitter.com/readthedocs/status/1603095976117522433>`_:

.. raw:: html

   <blockquote class="twitter-tweet"><p lang="en" dir="ltr">GeoPandas is an open source project to make working with <a href="https://twitter.com/hashtag/geospatial?src=hash&amp;ref_src=twsrc%5Etfw">#geospatial</a> data in <a href="https://twitter.com/hashtag/Python?src=hash&amp;ref_src=twsrc%5Etfw">#Python</a> easier. <a href="https://twitter.com/geopandas?ref_src=twsrc%5Etfw">@GeoPandas</a> extends the datatypes used by pandas to allow spatial operations on geometric types.<br><br>We want to highlight some things we love from their docs.<br><br>🤏 (small) 🧵 <a href="https://t.co/Hj82s6SDQP">pic.twitter.com/Hj82s6SDQP</a></p>&mdash; Read the Docs (@readthedocs) <a href="https://twitter.com/readthedocs/status/1603095976117522433?ref_src=twsrc%5Etfw">December 14, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Awesome Read the Docs Projects List 🕶️
--------------------------------------

Looking for more inspiration?
Check out our new list `Awesome Read the Docs Projects <https://github.com/readthedocs-examples/awesome-read-the-docs>`_
and help us discover more awesome projects.


Read the Docs for Business
--------------------------

Considering using Read the Docs for an organization?

.. raw:: html

   <a href="https://about.readthedocs.com/" style="background-color: #409cff; border-radius: 3px; color: #ffffff; display: block; margin: 30px auto; font-size: 18px; font-weight: 700; line-height: 24px; padding: 15px 0 15px 0; text-align: center; text-decoration: none; width: 238px;">
     Discover all the features ✨️
   </a>

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
