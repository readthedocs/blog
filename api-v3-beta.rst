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
we decided to make a bigger step forward and create our new shiny API v3 with better and nicer features,
putting the focus on the user cases we heard about from existing users.

Our new API v3 has some big differences compared to the old one that make it more user-friendly and useful.

These differences includes:

* Authenticated only
* Token based authentication
* Read and Write
* Project's slug resource based

Allowing us to build new good features on top of them, like:

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

APIv3 is currently in an invite-only Beta state on our Community site, https://readthedocs.org.
In case you want to test it and give us feedback on it,
please `email us`_ to get early access.

We plan to add more features based on the feedback we receive from you to cover most of the common use cases.
Please, help us with your feedback to make the new APIv3 *even* better!

.. _email us: support@readthedocs.org
