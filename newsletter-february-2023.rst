.. post:: Feb 1, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - February 2023
========================================

News and updates
----------------

Here are the latest updates from our team since the :doc:`previous newsletter </newsletter-january-2023>`:

- 🪄️ Build outputs are now stored in a well-known location, available to the build process.
  This opens up many new and exciting possibilities for generating and processing final output formats,
  which we will uncover in an upcoming blog post.
  PDFs for MkDocs and encrypted documentations are just two demos that we have ready.
  **Stay tuned!**
- 🌪️ Uploads are faster and done in parallel,
  thanks to `rclone`_. 
- 🔒️ CORS headers have been tightened on all platforms.
- 🛠️ The default branch of a git repository is now correctly detected in manual imports.
  This was a long-standing bug that we are very happy to finally have fixed.
- 🎤️ Write the Docs has announced their 2023 conferences.
  Read more in `their announcement <wtd_announcement>`_
- 🔒️ Security issue found and fixed: `Path traversal: access to files from any project <GHSA-5w8m-r7jm-mhp9>`_
- 🔒️ Security issue found and fixed: `Symlink following: Arbitrary file access from builder server <GHSA-hqwg-gjqw-h5wg>`_
- 🔒️ Security issue found and fixed: `Cache poisoning <GHSA-7fcx-wwr3-99jv>`_
- 🚦️ Note from Cloudflare that provides CDN for everything on readthedocs.io:

    On February 14th, 2023,
    Cloudflare will be doing database maintenance that will impact SSL API availability and may result in certificate issuance delays.
    The scheduled maintenance will be on February 14, 2023, 14:00 - 16:00 UTC.

.. _rclone: https://rclone.org/
.. _wtd_announcement: https://www.writethedocs.org/blog/2023-january-update/
.. _GHSA-5w8m-r7jm-mhp9: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-5w8m-r7jm-mhp9
.. _GHSA-hqwg-gjqw-h5wg: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-hqwg-gjqw-h5wg
.. _GHSA-7fcx-wwr3-99jv: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-7fcx-wwr3-99jv

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.


.. raw:: html

   <a href="https://about.readthedocs.com/" style="background-color: #409cff; border-radius: 3px; color: #ffffff; display: block; margin: 30px auto; font-size: 18px; font-weight: 700; line-height: 24px; padding: 15px 0 15px 0; text-align: center; text-decoration: none; width: 238px;">
     Discover all the features ✨️
   </a>

Upcoming features
-----------------

..
  Notes:

  Next newsletter:
  Make a general announcement of our Roadmap

  General:

  When creating newsletter drafts, we keep the items here from the previous newsletter.
  This is in order to ensure due follow-up on features that are announced publicly.
  
  Feature done? A great follow-up is to add what was previously an upcoming feature as a released feature in the former section.
  
  Feature not done?
  Make sure that upcoming features are announced with a link to issues or PRs where the progress can be seen.
  If this is done, then subsequent newsletters aren't compelled to share progress when it's uninteresting.
  
  If a feature was announced as upcoming but isn't yet released,
  then try rephrasing the announcement as a general news update about the progress and where it can be followed.

- Specific upcoming features from roadmap

Interested in all the details? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/4

Possible issues
---------------

* The change of the standard build output directory will cause issues for anyone that has custom builds and have guessed the old unofficial output directory.
  See technical details in: https://github.com/readthedocs/readthedocs.org/pull/9888
* If you want to use Sphinx 6 wth sphinx-rtd-theme,
  we will ship an update next week of both the new theme and an update on our platform dealing with the removal of jQuery from Sphinx.

Awesome Project of the month
----------------------------

TBD


Awesome Read the Docs Projects List 🕶️
--------------------------------------

.. Depending on interaction, maybe time to turn this into a link in the above section

Looking for more inspiration?
Check out our new list `Awesome Read the Docs Projects <https://github.com/readthedocs-examples/awesome-read-the-docs>`_
and help us discover more awesome projects.


-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
