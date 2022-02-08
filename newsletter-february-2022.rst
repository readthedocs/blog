.. post:: Feb 8, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features in February.

Read the Docs newsletter - February 2022
========================================

Welcome to the latest edition of our monthly newsletter, where we
share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company updates
---------------

- We have mostly finished migrating Read the Docs for Business users to Cloudflare for SSL.
  There are lots of interesting features this will enable,
  so stay tuned for updates there.
- We're sad to announce that `Juan Luis`_ has moved on from Read the Docs as our developer advocate.
  The work he did was vital towards getting our :doc:`CZI grant </czi-grant-announcement>` mostly finished, and we thank him for his time spent bettering the RTD, Sphinx, and docs community.
- On a related note, we're going to be hiring again soon to fill another position.
  It will be a bit different and likely a product-focused Python development position.
  If you're interested, please `let us know`_.

.. _let us know: mailto:hello@readthedocs.org?subject=Job%20Posting

New features
------------

In January we continued to work on refactors and internal changes.
Among the major user-facing changes:

- We fixed a bug in Bitbucket that didn't allow us to properly sync user permissions.
  This resulted in a few support requests, but has now been resolved.
- We improved our ability to mark projects as non-spam,
  so that we can validate a project isn't spam and then make sure it doesn't get flagged by our automated system.

You can always see the latest changes to our platforms in our :doc:`Read the Docs
Changelog <readthedocs:changelog>`.

Upcoming features
-----------------

- Cancelling a build is a long requested feature, and we're getting close to implementing it.
- We're looking at tracking 404 pages in our project analytics,
  so that projects can easily fix up missing or outdated page links.
- We are hoping to launch our revamped landing pages this month,
  which will give our front page a much needed refresh.
- We are working to define a policy for canonical docs and cloned versions,
  so that we can more easily remove outdated docs for projects.
- We're working to investigate supporting a CDN on Read the Docs for Business,
  which will be an exciting new feature for our users there.
- We're `looking at how to support <https://github.com/readthedocs/readthedocs.org/issues/8811>`_ multiple ``readthedocs.yml`` files in a single git repo.

Possible issues
---------------

We continue to see a good pace of development on the Sphinx project,
with them adding support for docutils 0.18,
and removing jQuery in a major refactor of their Javascript.
We're working to ensure that our theme and other parts of the ecosystem don't break with these changes,
and trying to be procative to address any possible issues.
That said,
there will likely still be some issues that sneak through with the release of Sphinx 4.5 (docutils upgrade) and Sphinx 5.0 (JS refactor).

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Ana: https://github.com/nienn
.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
