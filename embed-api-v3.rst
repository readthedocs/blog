.. post:: December 7, 2021
   :tags: api, feature, grant
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      We are thrilled to announce the availability of Read the Docs Embed API v3,
      along with its official client, sphinx-hoverxref 1.0.
      We invite the community to try them out and let us know their feedback.

Announcing Embed API v3 and sphinx-hoverxref 1.0
================================================

We are thrilled to announce the availability of Read the Docs Embed API v3,
along with its official client, sphinx-hoverxref 1.0.
This work has been possible in part thanks to the
:doc:`the CZI grant we received </czi-grant-announcement>`.

The value of content embedding
------------------------------

As we wrote in
:doc:`our first blog post about sphinx-hoverxref </hoverxref-intersphinx>`,
one of the most powerful features of Sphinx
is the possibility of creating cross references
to other documentation projects.
However, a reader finding several links in a technical documentation
might need to open several browser tabs to fully understand the context,
resulting in a lot of friction in the form of context switching.

One way of mitigating the problem is to show a small preview
in the form of tooltip or modal with the contents of the link.
This is where the Embed API and sphinx-hoverxref come in.

`sphinx-hoverxref`_ is a Sphinx extension that addresses this problem
by adding tooltips on the cross references of the HTML documentation
with the content of the linked section.
To do so, it inserts a small JavaScript file that
calls the Read the Docs Embed API when the user hovers any link.
:doc:`Back in June </hoverxref-intersphinx>` we announced
intersphinx support in `sphinx-hoverxref`_ 0.6b1,
which allowed users to include modals and tooltips
also for cross references to other projects.

.. figure:: img/sphinx-hoverxref-showcase.gif
   :width: 60%
   :align: center
   :alt: sphinx-hoverxref displaying tooltips for cross references
   :target: /_images/sphinx-hoverxref-showcase.gif

   sphinx-hoverxref displaying a tooltip including an equation

.. _sphinx-hoverxref: https://sphinx-hoverxref.readthedocs.io/

Some big projects already using it include `Tweepy <https://docs.tweepy.org/>`_,
a Python client for Twitter, and `Scrapy <https://docs.scrapy.org/>`_,
a framework for crawling websites.

Embed API v3 and sphinx-hoverxref 1.0
-------------------------------------

After some months of work, **we are excited to publish v3 of our Embed API,
and with it, version 1.0 of sphinx-hoverxref**.

Among other things,
the new versions allow you to
:ref:`embed content from pages hosted outside Read the Docs <guides/embedding-content:embedding content from your documentation>`.
For security reasons, we have an allowlist of such external domains
that currently includes Python, NumPy, SciPy, SymPy,
and we would like to
`invite the community to suggest more domains to add <https://github.com/readthedocs/readthedocs.org/issues>`_.

Other additions and fixes include:

- Support for JS and CSS assets in Sphinx 4.1+.
- Support for ``glossary`` / ``term`` and sphinxcontrib-bibtex.
- Avoid showing the browser built-in tooltip for links that have the extension enabled.

Finally, version 3 of the Embed API
paves the way for supporting non-Sphinx projects in the future.

Embedding content with sphinx-hoverxref
---------------------------------------

To use sphinx-hoverxref in your Read the Docs project,
:doc:`declare it as part of your dependencies <guides/reproducible-builds>`:

.. code-block::
   :caption: requirements.txt
   :emphasize-lines: 3

   sphinx==4.3.1
   sphinx_rtd_theme==1.0.0
   sphinx-hoverxref==1.0.0

And add it to your list of Sphinx extensions:

.. code-block::
   :caption: conf.py
   :emphasize-lines: 3

   extensions = [
       # ...other extensions
       "hoverxref.extension",
   ]

To enable the extension on all ``:ref:`` of your documentation,
set the ``hoverxref_auto_ref`` to ``True``:

.. code-block::
   :caption: conf.py

   hoverxref_auto_ref = True

And you will start seeing tooltips on your internal references.
Apart from ``:ref:`` roles, you can also enable tooltips on:

- :ref:`Code objects from any Sphinx domain <hoverxref:Usage:Tooltip on Sphinx Domains>`,
- :ref:`Glossary terms <hoverxref:Usage:Tooltip on glossary terms>`,
- :ref:`BibTeX citations <hoverxref:Usage:Tooltip on sphinxcontrib-bibtex cites>`,
- :ref:`Pages containing extra JavaScript like sphinx-tabs and
  MathJax <hoverxref:Usage:Tooltip with content that needs extra rendering steps>`,
- :ref:`Intersphinx references <hoverxref:Usage:Tooltip on intersphinx content>`,
- :ref:`And custom objects! <hoverxref:Usage:Tooltip on custom object>`

.. note::

   sphinx-hoverxref includes the JavaScript embed client in the HTML assets,
   but it is not yet available as a standalone library that can be reused
   with standard frontend packaging tools.
   If you would like to see this happening,
   `let us know <https://github.com/readthedocs/sphinx-hoverxref/issues/>`_.

Calling the Embed API directly
------------------------------

As explained in :ref:`our embedding
guide <guides/embedding-content:calling the embed api directly>`,
you can call the API directly from any HTTP client:

.. code-block:: console

   $ curl -s "https://readthedocs.org/api/v3/embed/\
   > ?url=https://docs.readthedocs.io/en/latest/features.html\
   > %23read-the-docs-features" | python -m json.tool
   {
     "url": "https://docs.readthedocs.io/en/latest/features.html#read-the-docs-features",
     "fragment": "read-the-docs-features",
     "content": "<div class=\"section\" id=\"read-the-docs-features\">\n<h1>Read the Docs ...",
     "external": false
   }

Or visually explore the query in the `web interface`__ instead.

.. __: https://readthedocs.org/api/v3/embed/?url=https://docs.readthedocs.io/en/latest/features.html%23read-the-docs-features

The :ref:`reference documentation <readthedocs:api/v3:embed>`
includes more detail about the parameters and return values of the API.

Try it out!
-----------

We would like to invite the community to try out these features and
send us feedback. With the help of our users, we will keep moving towards
a more cohesive documentation ecosystem of interlinked Python projects.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!
