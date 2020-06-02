.. post:: August 27, 2019
   :tags: api, feature, reference
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:

      Help us to make Read the Docs *even* better by joining our new API v3 invite-only beta!

========================
 Announcing API v3 Beta
========================

In the last months, we have been working on making our API better.
Considering the limitations of our current REST API v2,
we decided to make a bigger step forward and create a new API v3,
putting the focus on the use cases we heard about from existing users.

Compared to API v2, our new API v3 has some big differences that make it more user-friendly and useful.

These differences includes:

* API access requires authentication
* Token based API authentication
* Read and write
* Resource lookup can use project's slug
* Wider resource coverage

Some examples of new queries and actions that will be possible with the API are:

* :ref:`Import a new project <readthedocs:api/v3:Project create>`
* :ref:`List all my projects <readthedocs:api/v3:Projects list>`
* :ref:`Activate a version <readthedocs:api/v3:Version update>`
* :ref:`Trigger a build for a specific version <readthedocs:api/v3:Build triggering>`
* :ref:`Check build status <readthedocs:api/v3:Build details>`
* :ref:`Manage redirects <readthedocs:api/v3:Redirects>` and :ref:`environment variables programmatically <readthedocs:api/v3:Environment Variables>`

If you want to know more about it,
please check out the full `APIv3 documentation`_.

.. _APIv3 documentation: https://docs.readthedocs.io/page/api/v3.html


Invite-only beta feature
------------------------

APIv3 is currently in an invite-only beta state on our community site, https://readthedocs.org.
In case you want to test it and give us feedback on it,
please `email us`_ to get early access.

Based on the feedback we receive from you, we plan to add more features to cover most of the common use cases.
Please, help us with your feedback to make the new APIv3 *even* better!

.. _email us: support@readthedocs.org
