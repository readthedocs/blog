.. post:: June 23, 2020
   :tags: embed, sphinx, sphinx-extension, api
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      Read the Docs allows you to embed content from any of the projects we host.
      This allows reuse of content across sites, making sure the content is always up to date.


Embedding Content From Your Documentation
=========================================

We are excited to announce the release of content embedding.
This allows users to embed content from any of the projects we host, *anywhere*.
Our approach to embedding content is a very simple but powerful idea:
*return the content of a specific section from a particular document in a project*.

We have built an `Embed API`_ as the backend that powers this feature.
On top of this API,
we have built two improvements to the experience of our platform.

.. _Embed API: https://docs.readthedocs.io/en/latest/api/v2.html#get--api-v2-embed-

Contextualized tooltips on documentation pages
----------------------------------------------

Our first goal was adding extra context to a link within the same page.
This helps the reader understand a concept,
without switching context and jumping into another completely different page.

Documentation is already full of links to additional content,
and with the new Embed API that can return that exact content,
we thought *let's add a tooltip with this content when the reader hovers the link!*
That's how `sphinx-hoverxref`_ was born.

``sphinx-hoverxref`` allows documentation authors to easily add these tooltips,
customize their style, and decide which elements will show tooltips.
We recommend `reading the docs`_ to see everything it can do. 

.. figure:: /_static/sphinx-hoverxref-demo.gif

  Example of ``sphinx-hoverxref`` on Read the Docs documentation.

.. _sphinx-hoverxref: https://sphinx-hoverxref.readthedocs.io/
.. _reading the docs: https://sphinx-hoverxref.readthedocs.io/

Inline help on our application website
--------------------------------------

Adding too much copy in your application can be overwhelming to users,
meaning they don't read it.
We try to keep the application copy minimal, and link out to documentation when appropriate.
This pattern has worked fine over time, but it has the same problem of context switching to a completely different page.

Since we've started working on a new re-design of our entire application UI (more on this coming soon!),
we added the usage of the Embed API to add this extra documentation.
By adding a tooltip to our documentation links,
we allow the user to maintain the content in our application but also learn more about the features they are using.

In summary
----------

If you liked the Embed API and you would like to embed content from your documentation anywhere,
you can `read its full documentation`_ to learn more about it.

.. _read its full documentation: https://docs.readthedocs.io/en/stable/guides/embedding-content.html

We think it's a super powerful feature and we encourage you to use the extension we built on top of it,
or even better, build your own and share them with us!
