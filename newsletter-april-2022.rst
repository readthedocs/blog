.. post:: Apr 7, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - April 2022
=====================================

March has been a productive month for Read the Docs.
We have finished our :doc:`Product-focused Application Developer </job-product-developer/>` job posting,
which we're excited about.
We plan to share this on a few job boards,
and are looking for someone to join the team who is excited to work on our product.

New features
------------

We've continued building a number of features and bug fixes in our March roadmap:

- We now allow custom commands to run before and after your builds: ``build.jobs``. This is a long requested feature, so `check it out`_ now!
- We're testing Ubuntu 22.04 on our builders, which you can try by setting ``build.os: ubuntu-22.04`` in your ``.readthedocs.yaml`` file.
- We added a number of small improvements to the build process, making it easier to theme the resulting HTML with information about the versions built. Check out `all the options available`_.
- We've improved importing ``Project``'s via the API. They are now properly connected to your GitHub repository or similar, so we can use that for VCS SSO on Read the Docs for Business.
- We migrated all of our repositories to the ``main`` branch. This is a long-standing issues, and something we're happy to have finished.

You can always see the latest changes to our platforms in our :doc:`Read the Docs
Changelog <readthedocs:changelog>`.

.. _check it out: https://docs.readthedocs.io/en/latest/config-file/v2.html#build-jobs
.. _all the options available: https://docs.readthedocs.io/en/latest/builds.html#build-environment

Upcoming features
-----------------

- 404 tracking is coming soon, which will allow users to better understand what pages users are hitting that don't exist.
- We are working to increase the security of our build process, something that we continue to iterate on over time.
- Our roadmap has been moved to Github, and we're hoping to make it public here soon. This will allow users to get more insight into our development process, along with what we mention on the newsletter each month.

Possible issues
---------------

- There was an issue syncing your VCS repos when an organization had a large number of projects. We hope this has been fixed, but please let us know if it isn't.
- We are still watching Sphinx upgrades for possible issues they might cause around the ecosystem.
- We worked to mitigate a Jinja2 upgrade that caused issues last month, and continue to address some of the underlying fixes around dependencies.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _contact us: mailto:hello@readthedocs.org
