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
  if we get accepted.
  The funding would cover 2 years of work, starting in 2022.
- We keep making progress on the current CZI grant work:
  `Juan Luis`_ sent the first pull request for `our new Sphinx
  tutorial <https://github.com/sphinx-doc/sphinx/pull/9276>`_,
  which received positive feedback from the maintainers,
  and `Manuel`_ is about to release a new version of ``sphinx-hoverxref``
  `with support for intersphinx <https://github.com/readthedocs/sphinx-hoverxref/pull/86>`_
  (we will write a dedicated blog post about this soon).
- We added a `Data Processing Agreement <https://docs.readthedocs.io/en/stable/legal/dpa/>`_
  to our official documentation.
- We are iterating on an improved roadmap workflow to make sure our team
  stays productive as we grow.

New features
------------

- We added a new configuration key, ``build.apt_packages``,
  that allow our users to install custom operating system packages.
  You can read more `in our dedicated blog post </apt-packages>`_.
- Now redirects also work `if you are using
  HTTP <https://github.com/readthedocs/readthedocs.org/issues/8183>`_.

You can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_.

Upcoming features
-----------------

- `Anthony_` will keep working on our new UI templates
  as well as pushing ``sphinx_rtd_theme``,
  and continue assisting with the Frontend hiring process.
- `Eric`_ will continue to focus on improving the product for our Enterprise users.
  This includes working on auditing functionality, security process improvements,
  and other small features. He will also keep working on improving the ads platform.
- `Juan Luis`_ will continue writing the new Sphinx tutorial
  and scheduling Customer Development calls with scientific users,
  along with advertising more options for projects to remove ads.
- `Manuel`_ will wrap up the new sphinx-hoverxref release,
  continue working on SSO to make it discoverable by users,
  and keep pushing the Embed API v3 design document
  as well as new ideas for how our builders work.
- `Santos`_ will work on enabling pull request builds of commercial projects to be public,
  continue unifying our community and commercial codebases,
  and work with `Manuel`_ on defining our new philosophy for our builders,
  so we can move away from injecting logic on behalf of the users
  and improve the extensibility of our platform
  (see `our ongoing discussion <https://github.com/readthedocs/readthedocs.org/pull/8190/>`_).

Possible issues
---------------

After the recent news of `GitHub <https://github.blog/2021-04-22-github-actions-update-helping-maintainers-combat-bad-actors/>`_
and `GitLab <https://about.gitlab.com/blog/2021/05/17/prevent-crypto-mining-abuse/>`_
restricting their free offerings to prevent crypto mining abuse,
we started researching ways to detect and prevent
this situation from happening to us in the future.

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
