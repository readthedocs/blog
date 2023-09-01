.. post:: September 4, 2023
   :tags: newsletter, python
   :author: Anthony
   :location: GEG
   :category: Newsletter

Read the Docs newsletter - September 2023
=========================================

News and updates
----------------

- 🚀 :doc:`We started testing a new flyout menu </addons-flyout-menu-beta>`
  as part of our beta test for documentation addons.
  The beta test is currently limited to projects using the ``build.commands``
  configuration key.
  
- 🛣️ We continue to have a number deprecations in progress.
  We announced this month deprecations of :doc:`installing using system packages </drop-support-system-packages>`,
  :doc:`the configuration key build.image </use-build-os-config>`,
  and :doc:`installation of pinned versions of Sphinx and MkDocs </defaulting-latest-build-tools>`.
  Keep an eye on your email for any deprecation notifications,
  as we will continue to notify maintainers of projects that might be impacted.

- 🔐 A security advisory involving symlink abuse during project builds was raised and patched.

- 📉 Changes to our request handling resulted in a 30% reduction in response times for 404 error responses.

    .. figure:: /img/2023-september-404.png
       
       Request times for 404 handling have dropped 30% since last release.

- ✨ We upgraded our application to use Django 4.2

Upcoming changes
-----------------

- ⚠️  In line with :doc:`our deprecation plans for builds without a configuration file </migrate-configuration-v2>`,
  projects will be required to specify a configuration file on continue building their documentation starting September 25th.
  Our last brownout date is September 4th, lasting 48 hours.
  To avoid any problems building your project,
  ensure it has a configuration file before then.
- 🚢️ We will be continuing our work on for our beta test of `Read the Docs Addons <https://github.com/readthedocs/addons>`__.
  Our focus is still on improving the new flyout menu, search, and analytics.

Want to follow along with our development progress? `View our full Roadmap 📍️`_

.. _View our full Roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1
.. _reach out: https://readthedocs.org/support/

Possible issues
---------------

- ⚠️ Make sure to follow directions from notifications regarding deprecations.
  We have notified project maintainers for any project that could be affected by one of our ongoing deprecations.
  Updating your package ahead of brownout dates and final deprecation cutoff dates will ensure your project continues to successfully build.

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org

