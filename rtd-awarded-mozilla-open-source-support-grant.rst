.. post:: Dec 10, 2015
   :tags: funding
   :author: Anthony

Read the Docs Awarded Mozilla Open Source Support Grant
=======================================================

Several months back, Mozilla launched a new initiative -- the `MOSS`_ program --
to provide financial support to the open source software projects it relies on.
Mozilla allocated $1 million to the MOSS fund to provide grants for up to 10
projects matching the program's criteria.

Read the Docs is among the `first round of awards`_ made for the MOSS program.
Our proposed grant, for $48,000, is to build a separate instance that integrates
with the Python Package Index's upcoming website, `Warehouse`_. This integration
will provide automatic API reference documentation upon package release, with
authentication tied to PyPI and simple configuration inside the distribution.
API reference documentation on every release will be the starting point of this
work, prose documentation generation will be more difficult here, as not all
packages use Sphinx or rST for documentation.

Having consistent API reference documentation across all released distributions
will be an enormous benefit to the Python ecosystem. API reference documentation
will be found in a single space, with version specificity, and will be able to
be tightly inter-linked across projects. This is hopefully the start of work
that could benefit other communities as well, by putting more emphasis on usable
documentation and best documentation practices.

We are currently just into the planning stage for this work. We hope to have an
official roadmap planned out, and a detailed breakdown of the work involved, in
the coming weeks. This post will be followed up with a more detailed look at our
plan and the work required. Work on this grant will hopefully begin early in the
new year and will be spaced out throughout the year.

Funding open source software communities is still a difficult proposition for
most companies. We appreciate Mozilla's stance and commitment to open source and
can only hope more companies take note and learn how to put value on the health
of the communities they rely on.

.. _`MOSS`: https://wiki.mozilla.org/MOSS
.. _`Warehouse`: https://warehouse.python.org/
.. _`first round of awards`: https://blog.mozilla.org/blog/2015/12/10/mozilla-open-source-support-first-awards-made/
