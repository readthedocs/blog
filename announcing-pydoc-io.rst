.. post:: Nov 17, 2016
   :tags: pydoc, documentation, api, reference

Announcing pydoc.io beta
========================

Today we're excited to announce our latest project: https://pydoc.io.
This work was made possible by the :doc:`MOSS Grant </rtd-awarded-mozilla-open-source-support-grant>` from Mozilla.
Thanks to Mozilla for funding our time building this wonderful community resource.

About pydoc.io
--------------

Running Read the Docs,
we've always been proud of the documentation tooling that the Python community has.
We prioritize prose over API documentation listings,
and generally have a high standard of documentation in our projects.

There are a specific set of use cases that API reference documentation support,
and the Python community doesn't support them well.
Tools like http://godoc.org and http://rubydoc.info provide these for others languages,
and we now introduce http://pydoc.io as the Python community's version of that.

What is it?
-----------

Pydoc.io will eventually auto-generate API reference documentation for every package on PyPI.
Our beta release will support a limited set of packages that we are using for testing.
Over time we'll expand the tooling to automatically support generating docs for any package posted on PyPI.

Reference documentation is wonderful for folks who already know how a library works,
and simply want to use it.
It's also great for navigating and understanding the internals of a piece of code.
Giving them simple access to nicely rendered API documentation supports using and understanding libraries in a nicer way than reading code.
We're happy to build out these tools,
along with the wonderful prose tools we've always had with Sphinx itself.

Our progress and some context is tracked in `issue 1957 <https://github.com/rtfd/readthedocs.org/issues/1957>`_.

The tools
---------

This project is built on top of `Sphinx`_ at it's core.
On top of that,
we've layered a few different tools:

* `sphinx-autoapi`_ which is the tool that takes Python source files and turns them into rST.
   * Internally, this uses the `pydocstyle`_ AST parser, which we use for a parse-only representation of the Python files.
* `pydoc.io`_ is a Django application that is the actual web front-end and documentation building code.
* `sphinx-apitheme`_ is the Sphinx theme that powers the actual API listing pages.

The biggest piece to call out here is the parse-only documentation generation.
Sphinx's autodoc module,
and most Python documentation generators rely on importing the code to get docstrings.
As we've learned with Read the Docs,
this is quite impractical for a large set of libraries,
including the scientific ecosystem that heavily relies on C libraries.
**Building and supporting a parse-only API tool makes doc builds faster and more reliable.**

We have built on top of the ``pydocstyle`` AST,
but it looks like we'll likely have to build out our own AST traversal to retrieve all docstrings and construct declarations that we need to output.
We have looked into some of the `other AST options <https://github.com/davidhalter/jedi/issues/630>`_ in Python,
but haven't decided on what direction we want to go when building our own.

We have put a good deal of work into all these different pieces,
but there is still a lot of work to be done.

Give us feedback
----------------

**This is a very beta release**.
We have developed a few different sets of tools,
and would love your feedback.
In particular:

* Give us examples of API documentation patterns that you like. We'd like to incorporate powerful patterns into our theme. 
* Don't give us feedback on specific design issues with the theme, we're still working on it!
* Let us know if you have ideas about how we can improve the general usability of the documentation
* Let us know features that you wish the site had

Thanks
------

Thanks again to Mozilla,
who funded this work.
It wouldn't have been possible without them,
and we're happy they funded the initial development.
We're always looking at ways to make the ongoing maintenance sustainable,
so please reach out to us if you'd like to help with our efforts!


.. _Sphinx: https://github.com/sphinx-doc/sphinx
.. _pydocstyle: https://github.com/PyCQA/pydocstyle/
.. _pydoc.io: https://github.com/rtfd/pydoc.io
.. _sphinx-apitheme: https://github.com/rtfd/apitheme/
.. _sphinx-autoapi: https://github.com/rtfd/sphinx-autoapi/
