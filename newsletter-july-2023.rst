.. post:: July 6, 2023
   :tags: newsletter, python
   :author: Eric
   :location: BND
   :category: Newsletter

Read the Docs newsletter - July 2023
====================================

News and updates
----------------

- 🚀 We shipped support for customizing the URL path for projects and subprojects,
  allowing you to remove or customize the `/projects/` path on subprojects.
  This is enabled via Support request currently,
  and only on certain plans on Read the Docs for Business.
- 🛣️ Deprecations underway:
  We have a number of old feature deprecations underway. 
  The goal here is to reduce complexity of our build platform,
  and enable users to control their own builds via ``build.tools`` and ``build.commands`` instead of feature flags.
  Keep an eye on your email for any deprecation notifications that might impact your project.
- 📧️ Getting too many deprecation notifications?
  We added the ability to opt out of email notifications.
  You can configure this in your user profile settings.
- ✅️ New tool updates for all build tools,
  including the latest stable versions of Python, PyPy, Node.js, Rust and Go.
  See the documentation of the `build.tools <https://docs.readthedocs.io/page/config-file/v2.html#build-tools>`__ for more info.
- 📚️ A new documentation how-to for ``.readthedocs.yaml`` was started at `Write the Docs <https://www.writethedocs.org/>`__ and finished recently.
  Read it here: :doc:`readthedocs:config-file/index`.
- ⏩️ HTTP speedups: Several HTTP endpoints and CloudFlare configurations have been tweaked and are performing better.
- 🐛️ Bug fix: We are now 100% relying on search indexing by parsing HTML, instead of special Sphinx-only logic. This makes search a lot simpler and more consistent for our users.

Upcoming features
-----------------

- ⏩️ Our build process is receiving considerable improvements for larger Git repositories.
  The ``git clone`` and ``git fetch`` operations are tweaked,
  which results in significant speedups.
  For instance, the CPython project now fetches its Git repository at nearly 10x the speed of before.
  The change is being deployed soon to a few select projects and then gradually rolled out.
  For more details,
  see `issue #9736 <https://github.com/readthedocs/readthedocs.org/issues/9736>`__.

- 🚢️ We have concluded work on the first phase of our new `Read the Docs Addons <https://github.com/readthedocs/readthedocs-client>`__.
  Our Addons will be a single library for all the ways Read the Docs enhances documentation.
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

