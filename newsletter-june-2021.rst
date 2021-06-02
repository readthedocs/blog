.. post:: June 3, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features from June.

Read the Docs newsletter - June 2021
====================================

Welcome to a new edition of our monthly newsletter, where we
openly share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

- We applied to the next round of the CZI Essential Open Source Software for Science!
  Our proposal is even more ambitious than the previous one,
  and we are excited about the possibilities for our users
  if we finally get accepted.
- We keep making progress on the current CZI grant work:
  `Juan Luis`_ sent the first pull request for `our new Sphinx
  tutorial <https://github.com/sphinx-doc/sphinx/pull/9276>`_,
  which received positive feedback from the maintainers,
  and `Manuel`_ is about to release a new version of ``sphinx-hoverxref``
  `with support for intersphinx <https://github.com/readthedocs/sphinx-hoverxref/pull/86>`_
  (we will write a dedicated blog post about this soon).
- We added a `Data Processing Agreement <https://docs.readthedocs.io/en/stable/legal/dpa/>`_
  to our official documentation.
- We are making progress towards a new streamlined workflow
  that helps us while the company grows.

.. Pageviews stats obtained from Google Analytics, https://readthedocs.io property,
   and divided by the total number of days in the month

New features
------------

- We added a new configuration key, ``build.apt_packages``,
  that allow our users to install custom operating system packages.
  You can read more `in our dedicated blog post </apt-packages>`_.
- Now redirects also work `even if you are using
  HTTP <https://github.com/readthedocs/readthedocs.org/issues/8183>`_.

You can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_ and `Ethical Ad Server
Changelog <https://ethical-ad-server.readthedocs.io/page/developer/changelog.html>`_.

Current focus & known issues
----------------------------

[TBC]

Upcoming features
-----------------

- `Anthony_` will keep working on our new UI templates
  as well as pushing ``sphinx_rtd_theme``,
  and continue assisting with the Frontend hiring process.
- `Eric`_ will write a design document for audit tracking in our service,
  polish our internal workflow and methodology changes with `Anthony`_,
  and soften the CORS restrictions of our current Embed API.
- `Juan Luis`_ will continue writing the new Sphinx tutorial
  and scheduling Customer Development calls with scientific users,
  besides advertising more options for projects to remove ads.
- `Manuel`_ will wrap up the new sphinx-hoverxref release,
  continue working on SSO to make it discoverable by users,
  and keep pushing the Embed API v3 design document
  as well as new ideas for how our builders work.
- `Santos`_ will write a proposal to improve logging of structured telemetry
  and work with `Manuel`_ on defining the new builders.

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
