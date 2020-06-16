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

We are happy to announce we have built a solid Embed API.
You can use it to embed content from any of the project we host, *anywhere*.
The Embed API is a very simple but super powerful idea:
*returns the content of a specific section from a particular document in a project*.

This functionality brought us the ability to work in two different projects:


Contextualized tooltips on documentation pages
----------------------------------------------

We thought it would be awesome if we could add some extra context to a link within the same page.
This would help the reader to understand in a better way the concept linked,
without switching context and jumping into another completely different page,
and maybe getting lost or distracted with lot of new content in the document opened.

We had the concept already highlighted by a link,
we had the Embed API that could return the exact content of the referenced section...
*Let's add a tooltip with this content when the reader hovers the link!*
--and that's how `sphinx-hoverxref`_ was born.

``sphinx-hoverxref`` allows the author of the documentation to easily add these tooltips,
customize their style, decide which elements will show tooltips and more!

.. figure:: /_static/sphinx-hoverxref-demo.gif

  Example of ``sphinx-hoverxref`` on Read the Docs documentation.

.. _sphinx-hoverxref: https://sphinx-hoverxref.readthedocs.io/


Inline help on our application website
--------------------------------------

Usually, we think that adding a text in the UI is not great and we are tempted to avoid it if possible.
We try to reduce the words there and, in case the feature is big enough, add a link to the full documentation.
This pattern has worked fine over time, but it has the same problem of context switching to a completely different page.

Since we've started working on a new re-design of our entire application UI (more on this coming soon!),
we thought we could introduce the usage of the Embed API to add this extra documentation,
with small links next to the feature we want to explain without overloading UI
but giving the user the ability to have the exact contextualized paragraph for that particular feature.


In summary
----------

If you liked the Embed API and you would like to embed content from your documentation anywhere,
you can `read its full documentation`_ to learn more about it.

.. _read its full documentation: https://docs.readthedocs.io/en/stable/guides/embedding-content.html

We think it's a super powerful feature and we encourage you to use the extension we built on top of it,
or even better, build your owns and share them with us!
