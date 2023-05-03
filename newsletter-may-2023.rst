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
- 🔒️ Vulnerability fixed: `Session hijacking on Read the Docs for Business <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-4mgr-vrh5-hj8q>`__

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


.. Awesome project of the month
.. ----------------------------

.. Skipped

.. Tip of the month
.. ----------------

.. Skipped

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
