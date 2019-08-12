.. post:: August 8, 2019
   :tags: api, feature, reference
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:

      Announcing API v3 Beta as invite-only status. Help us to make it *even* better!

========================
 Announcing API v3 Beta
========================

In the last months, we have been working on making our API better.
Considering the limitations of our current REST API v2,
we decided to make a bigger step forward and create our new shiny API v3 with better and bigger features,
putting the focus on the user cases we heard about from existing users.

Compared to API v2, our new API v3 has some big differences that make it more user-friendly and useful.

These differences includes:

* API access requires authentication
* Token based API authentication
* Read and write
* Resource lookup can use project's slug

Some examples of new queries and actions that will be possible with the API are:

* `Import a new project`_
* `List all my projects`_
* `Activate a version`_
* `Trigger a build for a specific version`_
* `Check build status`_
* `Manage redirects`_ and `environment variables programmatically`_

.. _Import a new project: https://docs.readthedocs.io/page/api/v3.html#project-create
.. _List all my projects: https://docs.readthedocs.io/page/api/v3.html#projects-list
.. _Activate a version: https://docs.readthedocs.io/page/api/v3.html#version-update
.. _Trigger a build for a specific version: https://docs.readthedocs.io/page/api/v3.html#build-triggering
.. _Check build status: https://docs.readthedocs.io/page/api/v3.html#build-details
.. _Manage redirects: https://docs.readthedocs.io/page/api/v3.html#redirects
.. _environment variables programmatically: https://docs.readthedocs.io/page/api/v3.html#environment-variables

If you want to know more about it,
please check out the full `APIv3 documentation`_.

.. _APIv3 documentation: https://docs.readthedocs.io/page/api/v3.html


Invite-only Beta feature
------------------------

APIv3 is currently in an invite-only beta state on our community site, https://readthedocs.org.
In case you want to test it and give us feedback on it,
please `email us`_ to get early access.

Based on the feedback we receive from you, we plan to add more features to cover most of the common use cases.
Please, help us with your feedback to make the new APIv3 *even* better!

.. _email us: support@readthedocs.org
