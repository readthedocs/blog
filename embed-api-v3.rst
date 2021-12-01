.. post:: December 2, 2021
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

Why using content embedding?
----------------------------

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

Embed API v3 and sphinx-hoverxref 1.0
-------------------------------------

Even though some projects were already using it,
the extension used older versions of our Embed API,
and by that time we already had a plan to overcome some of its limitations.
Among other things, we wanted the Embed API to

- Support embedding content from pages hosted outside Read the Docs, and
- Avoid coupling with Sphinx internal format,
  and directly parse the HTML instead.

After some months of work, **we are excited to publish v3 of our Embed API,
and with it, version 1.0 of sphinx-hoverxref**.

To test the API directly, you can do

.. code-block:: console

   $ curl -s "https://readthedocs.org/api/v3/embed/\
   > ?url=https://docs.readthedocs.io/en/latest/features.html\
   > %23read-the-docs-features" | jq
   {
     "url": "https://docs.readthedocs.io/en/latest/features.html#read-the-docs-features",
     "fragment": "read-the-docs-features",
     "content": "<div class=\"section\" id=\"read-the-docs-features\">\n<h1>Read the Docs ...",
     "external": false
   }

Or visually explore the query in the `web interface`__ instead.

.. __: https://readthedocs.org/api/v3/embed/?url=https://docs.readthedocs.io/en/latest/features.html%23read-the-docs-features

Making the backend do the request has several advantages:

- It can return to the client only the fragment of interest, instead of
  the whole page, reducing processing times in the browser.
- It can cache the result, thanks to the generous support of CloudFlare.

Some big projects already using it include `Tweepy <https://docs.tweepy.org/>`_,
a Python client for Twitter, and `Scrapy <https://docs.scrapy.org/>`_,
a framework for crawling websites.

Current limitations
-------------------

We would like to invite the community to try out these features and
send us feedback. In particular, the current version still has some limitations
that we would like to address soon:

- For security reasons, we have an allowlist of external domains
  the Embed API works with. We would like to invite the community
  to suggest more domains to add there, and evaluate them case by case.
- The JavaScript embed client is included in the assets of `sphinx-hoverxref`_,
  but it is not yet available as a standalone library that can be reused
  with standard frontend packaging tools.

With the help of our users, we will keep moving towards
a more cohesive documentation ecosystem of interlinked Python projects.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!
