.. post:: Dec 6, 2022
   :tags: newsletter, python
   :category: Newsletter
   :author: Eric

Read the Docs newsletter - December 2023
========================================

News and updates
----------------

* We have shipped :doc:`single version projects </introducing-support-for-version-only-projects>` to allow projects to be versioned without having translations. This is a long-requested feature that we've excited to ship based on our Proxito refactor work.
* We improved our webhook security by :doc:`requiring a secret </security-update-on-incoming-webhooks>` to be configured for all webhooks. This will help prevent malicious actors from triggering builds and other actions.
* Work continues on `Addons <https://github.com/readthedocs/addons/>`_, where we've added support for explicit EthicalAds placements on documentation pages, and are working on a new interface for configuring Addons.

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

Upcoming changes
----------------

* We are working to expand the functionality of our `redirects feature <https://github.com/readthedocs/readthedocs.org/pull/10825>`_ to support more use cases. This work is close to shipping.
* We working on the `upgrade to our dashboard notification system <https://github.com/readthedocs/readthedocs.org/pull/10890>`_, so that users have more control and better context for on-site notifications.
* Our `beta dashboard <https://beta.readthedocs.org/dashboard/>`_ continues to be tested in public beta, and new functionality for Addons configuration will only be available in that new interface.

Want to follow along with our development progress? `View our full roadmap 📍️`_

.. _View our full roadmap 📍️: https://github.com/orgs/readthedocs/projects/156/views/1

Possible issues
---------------

* Users need to update their webhooks before January 31, 2024 if they are configured without a secret. All users who need to take action should have received email and site notifications about this. 

-------

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org

