.. post:: May 1, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM
   :category: Newsletter

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - May 2023
=====================================

News and updates
----------------

- 🚁️ The proxy application El Proxito that serves all of our documentation websites has a new version that's being slowly rolled out.
  Several projects are now served using its new URL resolver,
  which is faster and is receiving new features.
  We expect to roll it out on all projects soon.
- 🔎️ ...One of the new features is a better 404 page which has is rolled out on projects that has the new Proxity resolver.
- 💫️ We now support multiple ``.readthedocs.yaml`` files in the same repository.
  This is great for monorepos that have several documentation projects with different tooling.
  Read more about the feature :doc:`in our docs <readthedocs:guides/setup/monorepo>`.
- ⚙️ If you use ``build.commands`` in ``.readthedocs.yaml``,
  you are no longer required to have a ``build.tools`` section.
  We changed the validation for ``.readthedocs.yaml`` to accommodate projects that do not need any of the built-in tools exposed.
- 🐛️ Fixed: URLs on pull request builds were pointing to the build page,
  rather than the documentation preview.
  If a build is successful,
  the URL now points to the documentation preview.
- 🔒️ GHSA-4mgr-vrh5-hj8q ...

Upcoming features
-----------------

- 🚢️ We have concluded work on the version 1.0 of our new `readthedocs-client <https://github.com/readthedocs/readthedocs-client>`_.
  It's a universal client that enhances documentation for all documentation projects hosted on Read the Docs.
  We will start to use it on a few selected projects.
  If you are interested in having it enabled on your project,
  please reach out.

Want to follow along with our development progress? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1


.. Possible issues
.. ---------------

.. - TBD


Awesome project of the month
----------------------------

`Crate.io <https://crate.io/docs/crate/tutorials/en/latest//>`__ has integrated 15 Sphinx projects in the same website experience and written their own theme.
So they rightly deserve to be this month's addition to `Awesome Read the Docs Projects 🕶️ <https://github.com/readthedocs-examples/awesome-read-the-docs>`_.
See the highlights in the following
`Twitter thread <https://twitter.com/readthedocs/status/1643210113186951168>`__ or
`Mastodon thread <https://fosstodon.org/@readthedocs/110140385774009615>`_:

.. raw:: html

   <blockquote class="twitter-tweet"><p lang="en" dir="ltr">A recent addition to our list of awesome projects 🕶️: <a href="https://twitter.com/crateio?ref_src=twsrc%5Etfw">@crateio</a> <a href="https://twitter.com/crateio?ref_src=twsrc%5Etfw">@crateio</a> combines multiple documentation projects into the same website experience.<br><br>Oh, by the way, the <a href="https://twitter.com/crateio?ref_src=twsrc%5Etfw">@crateio</a> docs will turn 10 years old in July 🎂️<a href="https://t.co/4cQMj3SNx6">https://t.co/4cQMj3SNx6</a><br><br>Here is a 🤏 (small) 🧵 <a href="https://t.co/tqP1dH5czb">pic.twitter.com/tqP1dH5czb</a></p>&mdash; Read the Docs (@readthedocs) <a href="https://twitter.com/readthedocs/status/1643210113186951168?ref_src=twsrc%5Etfw">April 4, 2023</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


.. Tip of the month
.. ----------------

.. TBD

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
