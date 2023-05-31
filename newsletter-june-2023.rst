.. post:: June 1, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM
   :category: Newsletter

Read the Docs newsletter - June 2023
====================================

News and updates
----------------

- ⚠️ It will be required to use a ``.readthedocs.yaml`` configuration file.
  It's highly encouraged to add one already today.
  Read more about this change in :doc:`/migrate-configuration-v2`.
- 🎥️ All the talks from `Write the Docs Portland 2023 <https://www.writethedocs.org/conf/portland/2023/>`__ can now be watched for free:
  `Open the new playlist on Youtube <https://www.youtube.com/watch?v=EZJ0mk9Jj3s&list=PLZAeFn6dfHpneQPsDWa4OmEpgW4pNiaZ2>`__.
- 🐛️ Builds with multiline commands suffered from `a few bugs <https://github.com/readthedocs/readthedocs.org/issues/10103>`__ that are hopefully all fixed now.
  Thanks to everyone who helped out!
- 🐛️ `sphinx-rtd-theme 1.2.1 <https://sphinx-rtd-theme.readthedocs.io/en/stable/changelog.html>`__ has been released with an important bug fix that caused jQuery to not load in certain projects.
- 🔒️ A high-severity vulnerability has been fixed:
  `Write access to projects via API V2 (/api/v2/project/* endpoints) for any logged-in user <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-rqfv-8rrx-prmh>`__.

Upcoming features
-----------------

- 🚢️ We have concluded work on the first phase of our new `readthedocs-client <https://github.com/readthedocs/readthedocs-client>`_.
  The client will be a single library for all the ways Read the Docs enhances documentation from having a flyout menu
  to link to other versions, translations, or subprojects, to showing version warnings for folks browsing outdated docs
  to running ads on community projects.
  There will be integration points and APIs to customize all of these features in the new client.

  We will start to use it on a few selected projects.
  If you are interested in having it enabled on your project,
  please `reach out`_.

Want to follow along with our development progress? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1

Possible issues
---------------

Issues?


Awesome project of the month
----------------------------

The most recent addition to
`Awesome Read the Docs Projects 🕶️ <https://github.com/readthedocs-examples/awesome-read-the-docs>`__
is `Ray's documentation <https://docs.ray.io/>`__ 🕶️.

Ray is an open source project, consisting of several components that all have their own section in a combined documentation set.

See the highlights in the following
`Twitter thread <https://twitter.com/readthedocs/status/1663923671470047234>`__ or
`Mastodon thread <https://fosstodon.org/@readthedocs/110463989114312961>`__:

.. raw:: html

   <blockquote class="twitter-tweet"><p lang="en" dir="ltr">The most recent addition to our awesome projects list is Ray&#39;s documentation 🕶️.<br><br>Ray by <a href="https://twitter.com/anyscalecompute?ref_src=twsrc%5Etfw">@anyscalecompute</a> is an open source project, consisting of several components that all have their own section in a combined documentation set.<a href="https://t.co/9YGpJvYpFD">https://t.co/9YGpJvYpFD</a><br><br>Here is a 🤏 (small) 🧵 <a href="https://t.co/QElmmJetPB">pic.twitter.com/QElmmJetPB</a></p>&mdash; Read the Docs (@readthedocs) <a href="https://twitter.com/readthedocs/status/1663923671470047234?ref_src=twsrc%5Etfw">May 31, 2023</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 


.. Tip of the month
.. ----------------

.. Skipped

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
.. _reach out: https://readthedocs.org/support/

