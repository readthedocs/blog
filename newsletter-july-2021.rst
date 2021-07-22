.. post:: July 8, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features in July.

Read the Docs newsletter - July 2021
====================================

Welcome to a new edition of our monthly newsletter, where we
share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

- Eric_ presented the history of the company at the Upstream 2021 conference
  along with ideas for open source sustainability.
  You can read more about it in :doc:`our recent blog post </behind-the-scenes-2021-1>`.
- We revamped our `sustainability page <https://readthedocs.org/sustainability/>`_
  to clarify the ways in which you or your project can go ad-free.
- The first two parts of the Sphinx tutorial we are writing
  in the context of the :doc:`CZI grant </czi-grant-announcement>`
  were merged to the development branch,
  and will be publicly available soon in the official Sphinx documentation.
- We finalized the design of our upcoming
  `Embed API v3 <https://docs.readthedocs.io/en/stable/development/design/embed-api.html>`_,
  which will open up more possibilities of embedding content inside and outside Read the Docs.
  Watch this space for updates on the topic.
- One extra person will join our team as Frontend Developer.
  More details coming soon!

New features
------------

- We added a new functionality to rebuild a specific PR build.
  A small user experience improvement that we hope is useful to many of our users
  (see image below).
- We added a JSON schema of our configuration file to
  `JSON Schema Store <https://www.schemastore.org/json/>`_.
  If your editor has support for JSON schema,
  it will now give you autocompletion and linting for
  `our .readthedocs.yml <https://docs.readthedocs.io/en/stable/config-file/v2.html>`_.

.. figure:: /img/rebuild.png
   :align: center
   :width: 80%
   :alt: Link to rebuild a specific build

   Link to rebuild a specific build

Thanks to our external contributors `@mongolsteppe`_, `Florian Bruhin`_,
`Seth Falco`_, `Rémi Verschelde`_, `Chris Holdgraf`_, and `Maksudul Haque`_.

You can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_.

.. _@mongolsteppe: https://github.com/mongolsteppe
.. _Florian Bruhin: https://github.com/The-Compiler
.. _Seth Falco: https://github.com/SethFalco
.. _Rémi Verschelde: https://github.com/akien-mga
.. _Chris Holdgraf: https://github.com/choldgraf
.. _Maksudul Haque: https://github.com/saadmk11

Upcoming features
-----------------

- Anthony_ will focus on getting our Sphinx theme to support Sphinx 4.0
  along with our external contributor `Aaron Carlisle`_,
  finishing up the financial summary of 2020,
  and onboarding our new Frontend hire.
- Eric_ will continue working on our sales process
  and doing pull request reviews,
  along with managing other ongoing projects. 
  In addition, he will push forward the proposal to add audit tracking
  along with Manuel_.
- `Juan Luis`_ is now collaborating more closely with the Sphinx team
  and will submit the third part of our beginners tutorial.
  In addition, he will lead a documentation sprint at SciPy,
  and start working on an introductory tutorial for Read the Docs.
- Manuel_ has already started with the implementation of our Embed API v3
  and will continue working on it for the coming weeks,
  apart from improving our data backups
  and implementing the first pieces of our audit tracking.
- Santos_ will keep on working with the refactoring of our codebases
  so our commercial and community sites are easier to maintain.
  He will also write a new guide about how to use unsupported VCS platforms
  on Read the Docs.

.. _Aaron Carlisle: https://github.com/blendify

Possible issues
---------------

Our release from June 15th contains `a security advisory to our CSRF
settings <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-3v5m-qmm9-3c6c>`_.

On an unrelated note, we are receiving more support requests from our users
about some software versions in our Docker images,
and we have decided to give that work more priority.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
