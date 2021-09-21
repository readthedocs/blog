.. post:: September 2, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features in September.

Read the Docs newsletter - September 2021
=========================================

Welcome to the latest edition of our monthly newsletter, where we
share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

- We have published
  :doc:`the first release candidate of version 1.0.0 of our Sphinx theme </theme-release-100rc1>`,
  which adds support for recent versions of Sphinx and docutils among other things,
  and announced our future plans for it.
  Check out the linked blog post to know more.
  **Update**: We have released 1.0 to PyPI
- The :doc:`first part of the new Read the Docs tutorial <readthedocs:tutorial/index>`,
  which we wrote as part of :doc:`our CZI grant </czi-grant-announcement>`, is online!
  We hope that it serves as a better starting point for people seeking to learn how to use our platform.

New features
------------

- Commercial users can now `share specific versions of their
  projects <https://docs.readthedocs.io/en/stable/commercial/sharing.html>`_
  and `log out from the flyout
  menu <https://docs.readthedocs.io/en/stable/versions.html#logging-out>`_.
- We added the possibility for users to `remove themselves from a
  project <https://github.com/readthedocs/readthedocs.org/pull/8384>`_
  without having to ask an owner to remove them
  (as long as they are not the only owner of the project).
- We fixed `a small usability issue with our search-as-you-type
  box <https://github.com/readthedocs/readthedocs-sphinx-search/pull/93>`_,
  that ignored the first typed characters under certain circumstances.
- We have documented our `unofficial support for
  Gitea <https://github.com/readthedocs/readthedocs.org/pull/8402>`_,
  and made other minor documentation fixes.

Thanks to our external contributors `Mozi`_, `Maksudul Haque`_,
`Stefano Costa`_, and `Christian Clauss`_.

You can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_.

.. _Mozi: https://github.com/pzhlkj6612
.. _Maksudul Haque: https://github.com/saadmk11
.. _Stefano Costa: https://github.com/steko
.. _Christian Clauss: https://github.com/cclauss

Upcoming features
-----------------


- Ana_ will continue researching tools for conducting automated testing on our Sphinx theme,
  review pull requests corresponding to the 1.1 milestone,
  and make some small styling improvements to our documentation.
- Anthony_ will work with Ana_ on testing our Sphinx theme,
  in addition to resuming work on our new user interface
  and doing some financial updates.
- Eric_ will keep pushing updates on our Commercial landing page
  and continue working on our sales processes. He's also 
  working to continue building EthicalAds as well. 
- `Juan Luis`_ will continue working on our Read the Docs tutorial,
  improving our onboarding experience,
  and put our email marketing and on-site notifications to work.
- Manuel_ will finish the work on our new Docker images and build process,
  and keep designing our upcoming GitHub Application.
- Santos_ will implement a new Slack integration,
  work with Manuel_ on the GitHub Application,
  and build a user interface for audit tracking.

Possible issues
---------------

We have been `making changes to how we store cookies <https://github.com/readthedocs/readthedocs.org/pull/8304>`_
to make our site more secure.
This has caused some minor issues in certain web browsers
or to `users that were embedding private documentation pages inside an
iframe <https://github.com/readthedocs/readthedocs.org/pull/8422>`_.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Ana: https://github.com/nienn
.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
