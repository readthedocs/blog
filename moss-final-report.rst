.. post:: Aug 10, 2017
   :tags: moss, pydoc, funding

MOSS Final Report
=================

Last year,
we were given a :doc:`MOSS Award </rtd-awarded-mozilla-open-source-support-grant>` to work on improving the Python documentation ecosystem.
We :doc:`announced </announcing-pydoc-io>` the initial deployment last November,
and this is the retrospective post about how the project as a whole went.

This work is live at http://www.pydoc.io/ and on GitHub:

* https://github.com/rtfd/pydoc.io - the source code for the site
* https://github.com/rtfd/sphinx-autoapi - the source code for parse-only API generation
* https://github.com/rtfd/apitheme - A Sphinx theme for API docs (incomplete)

Pydoc.io was created to generate API documentation for all Python packages.
We have now generated over 17,000 sets of API documentation for packages uploaded to PyPI,
without executing a single line of Python code from those projects.
This is the primary goal of the project,
and it has been successful.

The original grant covered the following items,
which I'll talk about in more detail:

* Add to Read the Docs the ability to build documentation from a release tarball of code in addition to the existing ability to build it from a version control system.
* Add to Read the Docs the ability to generate API documentation by parsing the Python code rather than by importing it.
* Add automatic documentation generation to the next version of the Python Package Index, Warehouse (https://warehouse.python.org/) - both API documentation and Sphinx documentation.
* Build out a custom hosting infrastructure for a new domain (<package>.pythondocs.com) or (<package>.python.readthedocs.org).
* Appropriate testing of the new code, and supporting the Python community in using the new facility.

After talking through each point,
I'll cover a few higher level thoughts on the topic of grant funding open source services.

Add ability to build docs from a tarball
----------------------------------------

This was focused on adding the ability to work with tarballs (zip files) instead of Version Control systems to Read the Docs.
As we got further into the development,
we `realized <https://github.com/rtfd/readthedocs.org/issues/1957>`_ it would be simpler to just create a new code project,
instead of trying to adapt Read the Docs for this purpose.

We ended up creating the `pydoc.io <https://github.com/rtfd/pydoc.io>`_ project as a new Django application.
It explicitly works with PyPI to download packages,
and doesn't know anything about Version Control.

We did this for a number of reasons,
but the primary one was to enable contributions.
The Read the Docs codebase had *a lot* of complexity around VCS,
and that complexity makes it hard to work on.
We are hoping that development on Pydoc will be adopted by the community,
in a manner that Read the Docs hasn't been.
Keeping the project simple and easy to contribute to was a large goal here.

Creating an entirely new code base also required us to spend time starting from scratch.
Instead of leveraging our own modeling,
hosting,
and other infrastructure,
we have to create it all again from scratch.
This ate up a decent amount of time that could have otherwise been spent on development,
but I think it still makes more sense to do it this way.

Add ability to generate Sphinx documentation with parsing instead of importing Python code
------------------------------------------------------------------------------------------

This work has been mostly successful,
and lives in the `sphinx-autoapi <https://github.com/rtfd/sphinx-autoapi/>`_ project.

As covered in the initial grant proposal,
having a parse-only solution for API documentation is a useful tool in the Python community.
This allows us to generate API docs for arbitrary code that is published to PyPI,
without having to execute it.
However,
given Python's dynamic nature,
there will always be some subset of data that can only be gathered by running the code.

We have gotten the autoapi solution to a point where we consider it about 90% done,
and it is generally useful.
You can see it in action on any project that is published to Pydoc currently:

.. TODO: Better examples of cool functionality

* https://www.pydoc.io/pypi/invenio-admin-1.0.0b2/autoapi/ext/index.html
* https://www.pydoc.io/pypi/actappliance-0.3.2/index.html
* https://www.pydoc.io/pypi/pyote-1.4.dev0/index.html

Add automatic documentation generation as packages are published to PyPI
------------------------------------------------------------------------

This is the primary value of the Pydoc `source code <https://github.com/rtfd/pydoc.io>`_.
It is an implementation of a Django app that polls PyPI,
and generates API documentation for each package as it is published.
Currently we are only supporting the Wheel format,
and projects published on Python 3.
We view this as a way to get people to move their packages into the future.

We currently have over **10,000** versions published to Pydoc.
We have been live building API documentation since the release of the beta in November.

Testing of the new code, and support the community
--------------------------------------------------

We have written some good unit tests for the autoapi code,
but pydoc.io itself is not as well tested as it could be.
In terms of supporting the community,
that hasn't been happening since we haven't gotten much uptake in usage.
I'll cover this a bit more in the take aways below,
but there is a large amount of marketing that would need to happen in order for us to fulfill the full value of the project.

High Level Take Aways
---------------------

When we applied for the grant,
the idea was to extend the ability of Read the Docs and Sphinx.
In extending Read the Docs,
we have mostly failed.
We broke Pydoc out into its own project,
in order to make it much easier to contribute to.
**This means that little of the work has been contributed back to Read the Docs code itself.**
However,
we have done a lot of work around building extensions to Sphinx.
This is work that is more widely applicable to any Sphinx user,
which is more useful in general for the Python and programming community as a whole.

**Creating open source software and not telling people about it is not inherently valuable.**
We did work on the major aspects of the grant,
but we didn't have the energy or focus to actually spend time marketing the new tools we have created.
Originally when we took the grant,
we thought it would be part of Read the Docs,
and so would naturally get exposure that way.
Once the site was split out as a separate instance,
it become necessary to market that,
along with all the other work we were already doing. 

One of the things that we've struggled with in funding and sustainability is the fact that we are a service.
**We felt that we needed to ask MOSS for money to complete specific,
actionable features.**
What we really need is funding for operating the service (wearing a pager),
supporting our users (responding to issues on GitHub),
helping mentor new contributors (reviewing Pull Requests),
and other activities that don't have a flashy outcome.

**I think that one thing that would help here is an explicit MOSS track that covers services or sustaining maintenance.**
A lot of funding is geared towards new development and R&D,
and there needs to be more money out there for simply keeping things going.
That would have been the most valuable money that we could have taken,
and in the end,
building out new capacity ended up effectively being more of a distraction from our core project goals.

We also spent a good deal of time creating our own API theme: https://github.com/rtfd/apitheme.
We realized part of the way through development that we should focus on getting the basic project done,
and we could focus on nicer theming later.
This ate up a chunk of time that wasn't necessary,
but I think the vision for a dedicated Sphinx API doc theme is a good one.
This is another place where we could bring in the community to hopefully work towards a better outcome,
but needed to dedicate time for that activity.

In the end,
we're glad we got the experience doing this MOSS grant,
and know a lot more about doing something similar in the future.
