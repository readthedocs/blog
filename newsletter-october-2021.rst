.. post:: October 7, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features in October.

Read the Docs newsletter - October 2021
=======================================

Welcome to the latest edition of our monthly newsletter, where we
share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

- We have resumed sending our blog updates by email.
  You can `subscribe to our newsletter <https://landing.mailerlite.com/webforms/landing/p8b7z2>`_
  so you don't miss them.
- Version 3 of our Embed API is now implemented,
  thanks to :doc:`the CZI grant we received</czi-grant-announcement>`.
  We will give more details about it soon.
- We have reworked :doc:`our team page <readthedocs:team>`
  to give you a better idea of who we are and how we work at the company.

New features
------------

- You can now use :ref:`our newer build specification <readthedocs:config-file/v2:build>`
  that leverages a newer image based on Ubuntu 20.04
  and gives more control over the versions of
  Python, Node.js, Rust, and Go.
  Projects like `pypa/cryptography <https://github.com/pyca/cryptography/pull/6330>`_
  and `thebe <https://github.com/executablebooks/thebe/pull/472>`_
  are already using it,
  and we will make an announcement with more information soon.
- We have added a new section to our Dashboard that exposes user security logs.

.. figure:: /img/security-log.png
   :align: center
   :width: 80%
   :alt: Security logs

   Security logs

- We have added a button on the Analytics section to download all your data,
  so you are not limited by the last 30 days that we show.
- We have revamped our onboarding process.
  If you are new to Read the Docs, you can now
  `fork our template repository <https://github.com/readthedocs/tutorial-template>`_
  and follow :doc:`our tutorial <readthedocs:tutorial/index>`
  to learn how to use the platform.
  We plan to keep expanding the tutorial during the coming weeks.
- We have made :doc:`our how-to guides <readthedocs:guides/index>` more visible
  and simplified its categorization, in addition to other documentation improvements.

Thanks to our external contributors `Mozi`_ and `Dmitry`_.

You can always see the latest changes to our platforms in our :doc:`Read the Docs
Changelog <readthedocs:changelog>`.

.. _Mozi: https://github.com/pzhlkj6612
.. _Dmitry: https://github.com/mitya57

Upcoming features
-----------------

- Ana_ will work on the UI of our landing and marketing pages,
  while making progress with version 1.1 of our Sphinx theme.
- Anthony_ will resume work on our new product interface
  and wrap up some financial updates.
- Eric_ will focus on expanding our CDN functionality on the commercial site,
  as well as addressing some upcoming changes to how custom domains work on Read the Docs Community.
- `Juan Luis`_ will document several recent changes,
  such us the new build specification and our support for generic webhooks,
  and continue expanding our tutorial and improving the SEO of our docs.
- Manuel_ will finish the migration of our services to Ubuntu 20.04,
  release a new version of sphinx-hoverxref that uses our new embed API,
  and gather feedback on our new build specification.
- Santos_ will continue consolidating our Community and Commercial codebases,
  finish the work on generic webbooks for easier integration with Slack and other tools,
  enable Commercial users to create new subscriptions after they cancel,
  and collaborate with Eric_ on the CDN issues.

Possible issues
---------------

We are detecting an increasing number of spammy projects on our platform.
While this rarely affects legitimate users, it is still a concern to us
and we are planning to take measures to tackle it.

In addition, some projects experienced networking issues due to
`the expiration of Let's Encrypt root certificate <https://github.com/readthedocs/readthedocs.org/issues/8555>`_.
We deployed a fix shortly after the problem was reported.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Ana: https://github.com/nienn
.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
