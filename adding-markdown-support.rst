.. post:: Oct 16, 2015
   :tags: commonmark, markdown, feature

Read the Docs & Sphinx now support Commonmark
=============================================

Read the Docs is built on top of Sphinx, 
which has always relied on reStructuredText as an input mechanism.
We have long heard from folks that they want to write documentation in Markdown,
as well as RST.

Today we are announcing that this is now possible!
With the standardization of Markdown into `Commonmark`_,
we have the ability to support a markup language with a proper spec.
`recommonmark`_ is the bridge that allows Commonmark to be used inside Sphinx.
**This allows you to use both RST and Commonmark inside of your Sphinx project.**

.. _Commonmark: https://commonmark.org/
.. _recommonmark: https://github.com/rtfd/recommonmark

Get started
-----------

We have documented how to :ref:`get started <readthedocs:intro/getting-started-with-sphinx:Using Markdown with Sphinx>` with Commonmark inside of Sphinx.
You simply::

    pip install recommonmark

Then in your ``conf.py``:

.. code-block:: python

    from recommonmark.parser import CommonMarkParser

    source_parsers = {'.md': CommonMarkParser}

    source_suffix = ['.rst', '.md']

This allows you to write both ``.md`` and ``.rst`` files inside of the same project.

Example Project
---------------

You can see this in action in my `sphinx-markdown-test repo`_ on GitHub.
You can also see a `rendered version`_ hosted on Read the Docs.

.. _sphinx-markdown-test repo: https://github.com/ericholscher/sphinx-markdown-test
.. _rendered version: https://sphinx-markdown-test.readthedocs.org/en/latest/

How it works
------------

The way this project works is that it allows Commonmark files to be parsed into `docutils nodes`_.
That means that everything downstream of the parser works the same as if the content came from RST.
This allows the content to slot into Sphinx and other RST based tools without much effort.

There are some caveats where certain Sphinx & docutils directives depend on the internal structure of RST.
We would like to eventually build a bridge from Commonmark to the Sphinx directives,
which would give a lot of the power of Sphinx to the Commonmark content.

We are looking at ways to handle this in the future,
and hope to eventually bring the full power of RST and Sphinx into the Commonmark ecosystem. 

.. _docutils nodes: http://docutils.sourceforge.net/docs/ref/doctree.html

Limitations
-----------

It should be noted that Commonmark doesn't support a lot of the concepts that RST lets you represent.
In particular,
there is no standardized way in Commonmark to represent inline or block levels constructs.
So things like the ``toctree`` directive and ``:ref:`` markup don't have an analog.

There is a `proposed draft`_ to the Commonmark spec to allow a similar syntax.
We are investigating adding support to this in recommonmark,
but we don't want to implement a standard prematurely.

Intended Usage
--------------

We think that Sphinx's power to reference code and other programming concepts is quite powerful.
However,
all content doesn't need this ability.
When you're writing content that just needs to have basic text formatting and links,
Commonmark is a great option for this.

We imagine that API reference documentation will continue to be authored in RST for quite some time.
Also index pages and other reference heavy content will continue to be RST.
FAQ's, blog posts, and other less reference heavy content is a great candidate for writing in Commonmark.

Feedback
--------

This is a new release,
so there are likely some missing pieces to our integration.
Go ahead and try it out.
Please file features ideas and bug reports on the `recommonmark bug tracker`_.

.. _proposed draft: http://talk.commonmark.org/t/generic-directives-plugins-syntax/444
.. _recommonmark bug tracker: https://github.com/rtfd/recommonmark/issues
