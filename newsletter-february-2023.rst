.. post:: Feb 7, 2023
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

- 🪄️ Build outputs are now stored in a well-known location: ``_readthedocs/<format>``.
  This opens up many new and exciting possibilities for generating and processing final output formats,
  which we will uncover in an upcoming blog post.
  *PDFs for MkDocs* and *encrypted documentation* are just two demos that we have ready.
  **Stay tuned!**
- 🌪️ Uploads are faster and done in parallel,
  thanks our migration to `rclone`_ which is in staged deploy to ensure availability. 
- 🔒️ Cross site requests to our approved API endpoints now reject requests that include credentials (cookies).
  This functionality was not needed,
  and had the potential for future security issues.
- 🛠️ The default branch of a Git repository is now correctly detected in manual imports.
  This was a long-standing bug that we are very happy to fix.
- 🔒️ Security issue found and fixed: `Path traversal: access to files from any project <GHSA-5w8m-r7jm-mhp9>`_
- 🔒️ Security issue found and fixed: `Symlink following: Arbitrary file access from builder server <GHSA-hqwg-gjqw-h5wg>`_
- 🔒️ Security issue found and fixed: `Cache poisoning <GHSA-7fcx-wwr3-99jv>`_
- 🎤️ Write the Docs has announced their 2023 conferences.
  Read more in `their announcement`_.

.. _rclone: https://rclone.org/
.. _their announcement: https://www.writethedocs.org/blog/2023-january-update/
.. _GHSA-5w8m-r7jm-mhp9: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-5w8m-r7jm-mhp9
.. _GHSA-hqwg-gjqw-h5wg: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-hqwg-gjqw-h5wg
.. _GHSA-7fcx-wwr3-99jv: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-7fcx-wwr3-99jv

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.


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

- More internal components of the build process will have a public API, giving full control and flexibility and allowing for more documentation tools to be used.
- Our Diátaxis documentation refactor is entering final stages before the first reveal.

Interested in all the details? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1

Possible issues
---------------

- 🚦️ There is a schedule maintenance window on Cloudflare that provides our CDN and SSL provisioning. 
  We are working to ensure that nothing is offline other than creation of new domains:

    On February 14th, 2023,
    Cloudflare will be doing database maintenance that will impact SSL API availability and may result in certificate issuance delays.
    The scheduled maintenance will be on February 14, 2023, 14:00 - 16:00 UTC.

- The change of the standard build output directory will cause issues for anyone that has custom builds and have guessed the old unofficial output directory.
  See technical details in `readthedocs.org#9888`_
- If you want to use Sphinx 6 with sphinx-rtd-theme,
  we have shipped an update of both the new theme and an update on our platform dealing with the removal of jQuery from Sphinx.
  See also :doc:`/sphinx6-upgrade`.
- In relation to the former update, we removed an injection of a legacy setting ``html_theme_path`` used with very old versions of Sphinx ``<1.6``.
  Please make note of this in case you are building documentation with this version of Sphinx.
  The recommended fix for the issue is to upgrade your Sphinx version.

.. _readthedocs.org#9888: https://github.com/readthedocs/readthedocs.org/pull/9888


.. Skipped in february
.. Awesome Project of the month
.. ----------------------------

Awesome Read the Docs Projects 🕶️
---------------------------------


**Looking for more inspiration?**
We continue building `Awesome Read the Docs Projects 🕶️ <https://github.com/readthedocs-examples/awesome-read-the-docs>`_,
a list full of inspirational documentation projects.

Please feel invited to open an issue or pull request in the repository with your suggestions.


-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
