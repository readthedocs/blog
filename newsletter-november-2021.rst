.. post:: November 4, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features in November.

Read the Docs newsletter - November 2021
========================================

Welcome to the latest edition of our monthly newsletter, where we
share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

- During the first week of November we attended the
  2021 Essential Open Source Software for Science Annual Meeting,
  an event organized by the CZI Science team.
  We are thrilled to connect with projects in the Open Science ecosystem.
- We upgraded our systems to Python 3.8 and Ubuntu 20.04 LTS.
  This will allow us to leverage newer Python features
  and use more up to date dependencies.
- :doc:`The Read the Docs tutorial <readthedocs:tutorial/index>` we started writing
  as part of :doc:`the CZI grant we received </czi-grant-announcement>`
  is now complete! We plan to keep updating it with user feedback
  and keep improving other parts of our documentation.

New features
------------

- We added `a checkbox to subscribe to our newsletter on new
  signups <https://github.com/readthedocs/readthedocs.org/pull/8546>`_.
  If you haven't already, you can also subscribe
  using the form on the top right of our blog.
- We `no longer show the rebuild option on closed or merged pull request
  builds <https://github.com/readthedocs/readthedocs.org/pull/8590>`_.
- We now `re-sync VCS accounts for SSO organization
  daily <https://github.com/readthedocs/readthedocs.org/pull/8601>`_.

Thanks to our external contributors `Adam Dangoor`_, `Arthur Milchior`_,
`Carlton Gibson`_, `Deepto`_, `Jürgen Gmach`_, and `Maksudul Haque`_.

You can always see the latest changes to our platforms in our :doc:`Read the Docs
Changelog <readthedocs:changelog>`.

.. _Adam Dangoor: https://github.com/adamtheturtle
.. _Arthur Milchior: https://github.com/Arthur-Milchior
.. _Carlton Gibson: https://github.com/carltongibson
.. _Deepto: https://github.com/deepto98
.. _Jürgen Gmach: https://github.com/jugmac00
.. _Maksudul Haque: https://github.com/saadmk11

Upcoming features
-----------------

- Ana_ will be working on bringing the mockups of our new landing pages to reality.
- Anthony_ will keep working on finances and taxes,
  and helping Ana_ with the frontend work.
- Eric_ will send out a report for our grant work,
  and work with Santos_ on implementing CloudFlare for our corporate site.
- `Juan Luis`_ will work on moving our development documentation to a separate project,
  finish the Sphinx tutorial, spread the word about MyST Markdown,
  and promote our Embed API.
- Manuel_ will add mechanisms to fight spam in our platform
  and improve our internal metrics.
- Santos_ will wrap up the custom outgoing webhooks
  and keep unifying the code of our community and commercial sites.

Possible issues
---------------

The docutils 0.18 release from late October is incompatible with older versions of Sphinx,
which are still used by a significant number of projects on Read the Docs.
A large number of them were not pinning their dependencies and have experienced broken builds,
which has resulted in a large number of issues and support requests.
We have written a blog post :doc:`explaining the situation and the ways to solve
it </build-errors-docutils-0-18>`.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Ana: https://github.com/nienn
.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
