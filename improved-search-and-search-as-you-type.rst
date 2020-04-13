.. post:: August 13, 2019
   :tags: gsoc, search, feature, in-doc-search, analytics
   :author: Vaibhav
   :location: LKO

GSOC 2019: Improved Search Results and Search As You Type
=========================================================

Giving users the ability to easily find the information that they
are looking for has always been important for Read the Docs.
This year, I, `Vaibhav Gupta`_, took the opportunity provided
by Google Summer of Code to improve the search.
The main goals of my `GSoC project`_ were:

- to make a `Sphinx extension`_ to provide "search you type" experience to the users.
- to add support for multiple hits per search result.
- to improve the UI/UX around code search.
- to add support for search analytics.

Search as you type feature is live on our docs.
You can go through these links to experience it:

- https://docs.readthedocs.io/?rtd_search=contributing
- https://docs.readthedocs.io/?rtd_search=api/v3/projects/

Google Summer of Code
---------------------

Google Summer of Code is a global program where students work with
an open source organization on a 3-month programming project.
I got accepted in the program and was excited to spend my summer with Read the Docs.

I have worked full time during the GSoC coding period and implemented various features.
All of my search related work can be seen in the `In-Doc Search UI Project Board`_.

Background
----------

The search code was originally contributed by `Rob Hudson`_,
`back in 2013`_ and then improved upon by other contributors.
It was greatly improved and upgraded by `Safwan Rahman`_ during :doc:`GSoC'18 </search-improvements>`.
Continuing on the same path,
I have implemented some new features on top of the existing search backend.

New Features
------------

During the GSoC period, I have worked on the following features:

- **In-Doc Search UI**: `readthedocs-sphinx-search`_ is a sphinx extension that adds a clean and minimal
  search UI to your docs. It supports "search as you type" feature.
  So, it is now possible to get instant results without being redirected to any other page.
  Read the docs `here`_.

.. figure:: /_static/in-doc-search-demo.gif
    :width: 100%
    :align: center
    :target: /_static/in-doc-search-demo.gif
    :alt: In-doc search ui demo

    In-Doc Search UI Demo

- **Multiple Hits Per Search Result**: This is one of the highly requested features.
  We now support search results from the sections of the docs, clicking on which will take you
  to that particular section and not just to the top of the result page.

- **Code Search**: We now support code search. If you want to search a particular function
  or an API endpoint -- you can just type your query and you will find it in the results.
  Eg: ``api/v3/`` or ``module.function``.

- **Search Analytics**: We now have support for search analytics.
  These analytics makes it easy to know what the users are looking for in your documentation.
  You can see these analytics in your project admin dashboard.
  Currently, this feature is in beta state and is available under a `feature flag`_.
  We plan to make this available for everyone soon.
  If you want to test this feature out and help giving us feedback,
  please contact us via `GitHub issues`_.

.. figure:: /_static/search-analytics-demo.png
    :width: 60%
    :align: center
    :target: /_static/search-analytics-demo.png
    :alt: Search analytics in project admin dashboard

    Search analytics demo dashboard

What Next?
----------

We don't intend to stop just yet.
We are planning to work on some more cool features in the near future,
some of which are:

- **Search Facets**:
  Facets can be used to make search more accurate.
  For example: In `Celery docs`_, facets can be used to search inside `Kombu docs`_ for "serializers",
  like ``subproject: kombu serializers``.
  (`readthedocs/readthedocs.org#5966`_)
- **Search Results Ordered By Most Viewed Pages**:
  It would be much more useful if the most viewed pages are shown first in the search results.
  (`readthedocs/readthedocs.org#5968`_)
- **Search Inside Sections**:
  It would be good if users have the option to get the
  search results from a particular section of the documentation.
  For example: Getting results from only `Guides`_ of our `documentation`_.
  (`readthedocs/readthedocs-sphinx-search#23`_).

Contributors Wanted
-------------------

As Read the Docs is an open source project backed by a small team of developers,
most of them are busy just keeping the site up and running.
Therefore, it's quite hard for them to take time to implement new features.
If you know some bit of Django or Python and Elasticsearch,
you can contribute to the search functionality of Read the Docs.
If you need any support to start contributing,
you can get in touch with me or any member of Read the Docs team.
You can find all of us at *#readthedocs* freenode IRC channel or `readthedocs gitter`_ channel.
I am *dojutsu-user* at IRC and *@dojutsu-user* at gitter.

Conclusion
----------

These new features will make it much easier to find the relevant information in the docs.
There are an infinite number of ways it can be improved and I believe we can compete
with major search engines in terms of documentation searching.
We don’t need superhero or coding guru, just need people who understand Python,
Django and Elasticsearch and have some time to write some code for us.
You are a **Superhero** to us if you can lend your time and effort to improve Read the Docs.


.. _Vaibhav Gupta: https://github.com/dojutsu-user
.. _GSoC project: https://summerofcode.withgoogle.com/projects/#5465587940065280
.. _Sphinx extension: https://readthedocs-sphinx-search.readthedocs.io/en/latest/
.. _In-Doc Search UI Project Board: https://github.com/orgs/readthedocs/projects/7
.. _Rob Hudson: https://github.com/robhudson
.. _back in 2013: https://github.com/readthedocs/readthedocs.org/pull/493
.. _Safwan Rahman: https://github.com/safwanrahman
.. _readthedocs-sphinx-search: https://github.com/readthedocs/readthedocs-sphinx-search
.. _here: https://readthedocs-sphinx-search.readthedocs.io/en/latest/
.. _feature flag: http://docs.readthedocs.io/page/guides/feature-flags.html
.. _GitHub issues: https://github.com/readthedocs/readthedocs.org/issues/new
.. _Celery docs: http://docs.celeryproject.org/en/latest/
.. _Kombu docs: http://docs.celeryproject.org/projects/kombu/en/latest/
.. _readthedocs/readthedocs.org#5966: https://github.com/readthedocs/readthedocs.org/issues/5966
.. _readthedocs/readthedocs.org#5968: https://github.com/readthedocs/readthedocs.org/issues/5968
.. _Guides: https://docs.readthedocs.io/page/guides/
.. _documentation: https://docs.readthedocs.io/
.. _readthedocs/readthedocs-sphinx-search#23: https://github.com/readthedocs/readthedocs-sphinx-search/issues/23
.. _readthedocs gitter: https://gitter.im/rtfd/readthedocs.org
