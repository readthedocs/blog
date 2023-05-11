.. post:: May 1, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM
   :category: Newsletter

Read the Docs newsletter - May 2023
===================================

News and updates
----------------

- 🚁️ The proxy application El Proxito has been rewritten and the new version is rolled out to selected projects.
  The application resolves URLs for all documentation websites hosted on Read the Docs.
  The new rewrite improves the performance of the resolver and makes it possible to add planned features.
  We are implementing these changes gradually,
  while monitoring their stability.
- 🔎️ ...One of the new features that have been added,
  is an improved 404 page,
  which contains better error messages and tips for users and project owners.
  It is available to projects using the new Proxito implementation.
- 💫️ We now support multiple ``.readthedocs.yaml`` files in the same repository.
  This is especially useful for *monorepos* containing multiple documentation projects with different configurations.
  This allows for instance configurations of several projects with different documentation tools and build environments.
  Read more about the feature :doc:`in our docs <readthedocs:guides/setup/monorepo>`.
- ⚙️ If you use ``build.commands`` in ``.readthedocs.yaml``,
  you are no longer required to have a ``build.tools`` section.
  We changed the validation for ``.readthedocs.yaml`` to accommodate projects that do not need any of the built-in tools exposed.
- 🐛️ Fixed: URLs on pull request builds were pointing to the build page,
  rather than the documentation preview.
  If a build is successful,
  the URL now points to the documentation preview.
- 🔒️ Vulnerability fixed: `CAS session hijacking on Read the Docs for Business <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-4mgr-vrh5-hj8q>`__

Upcoming features
-----------------

- 🚢️ We have concluded work on the first phase of our new `readthedocs-client <https://github.com/readthedocs/readthedocs-client>`_.
  It's a universal client that enhances documentation for all documentation projects hosted on Read the Docs.
  We will start to use it on a few selected projects.
  If you are interested in having it enabled on your project,
  please reach out.
- 🚁️ As mentioned earlier,
  we have rewritten our proxy application El Proxito and will start to add new features.
  One of the features being worked on is the ability to serve :doc:`subprojects <readthedocs:subprojects>` at custom URL paths.

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
