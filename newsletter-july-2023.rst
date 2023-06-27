.. post:: July 1, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM
   :category: Newsletter

Read the Docs newsletter - July 2023
====================================

News and updates
----------------

- 🛣️ Deprecations underway:
  The Read the Docs platform is sustainable for lots of future innovation.
  We have started a systematic approach to our deprecation process,
  and we are now able to deprecate features efficiently and with a clear migration path for everyone involved.
- 📧️ Getting too many deprecation notifications?
  We added the ability to opt out of email notifications.
- ✅️ New tool updates for all build tools,
  including the latest stable versions of Python, pypy, Node.js, Rust and Go.
  See the documentation of the `build.tools <https://docs.readthedocs.io/en/latest/config-file/v2.html#build-tools>`__ configuration option.
- 📚️ A new documentation how-to for ``.readthedocs.yaml`` was initiated at `Write the Docs <https://www.writethedocs.org/>`__ and finished afterwards.
  Read it here: :doc:`readthedocs:guides/setup/configuration-file`.
- ⏩️ HTTP speedups: Several HTTP endpoints and CloudFlare configurations have been tweaked and are performing better.
- 🐛️ Bug fix: We are now 100% relying on search indexing by parsing HTML with special-made heuristics. We removed a double-indexing that was caused by old Sphinx-oriented indexing.

Upcoming features
-----------------

- ⏩️ Our build process is receiving considerable improvements for larger Git repositories.
  The ``git clone`` and ``git fetch`` operations are tweaked,
  which results in significant speedups.
  For instance, the cpython project now fetches its Git repository at nearly 10x the speed of before.
  The change is being deployed soon to a few select projects and then gradually rolled out.
  For more details,
  see `issue #9736 <https://github.com/readthedocs/readthedocs.org/issues/9736>`__.

- 📚️ Multiple PDF support: We heard you!
  A 7 year old request for Multiple PDF support is being implemented and will support both Sphinx configurations and any other build tools that output multiple PDFs.
  Follow the progress in `issue #2045 <https://github.com/readthedocs/readthedocs.org/issues/2045>`__.

.. Skipped in May and June:

- 🚢️ We have concluded work on the first phase of our new `readthedocs-client <https://github.com/readthedocs/readthedocs-client>`__.
  The client will be a single library for all the ways Read the Docs enhances documentation from having a flyout menu
  to link to other versions, translations, or subprojects, to showing version warnings for folks browsing outdated docs
  to running ads on community projects.
  There will be integration points and APIs to customize all of these features in the new client.

  We will start to use it on a few selected projects.
  If you are interested in having it enabled on your project,
  please `reach out`_.

Want to follow along with our development progress? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1
.. _reach out: https://readthedocs.org/support/

Possible issues
---------------

- ⚠️ Please make sure to read the blog post: :doc:`/migrate-configuration-v2`.

  If you didn't have a ``.readthedocs.yaml`` configuration file,
  and you are introducing one for the first time,
  we're excited for you to be able to use all our new features like specifying build tool versions (Node, Rust, etc.)!
  
  The blog post offers help with that 💡️

Awesome project of the month
----------------------------

We are adding new entries to the list of `Awesome Read the Docs Projects 🕶️ <https://github.com/readthedocs-examples/awesome-read-the-docs>`__.
Feel free to open an issue or pull request if you've seen something that might inspire others.

This month's addition is `the developer documentation for django-cms <https://docs.django-cms.org/>`__,
which is noted for being both extremely extensive and well-organized at the same time.
It uses the `Furo <https://pradyunsg.me/furo/quickstart/>`__ theme that has full integration with Read the Docs' reader extensions.

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org

