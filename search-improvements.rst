.. post:: August 14, 2018
   :tags: gsoc, search, feature
   :author: Safwan
   :location: DHA

Improved Search
==================================
Have you ever used the search functionality inside documentations hosted by Read The Docs?
Mostly yes. Search can always be improved and in the era of Search Engines, the
documentation search also plays a big role for the users. The Read The Docs `core team`_
has realized the importance, and got me to take the challenge as a Google Summer of Code student.
The main goal of my GSoC project was to refactor the search code together with upgrading the backend
Search engine, as well as adding more features to the search functionality like exact match search,
case insensitive search, search as you type, suggestions etc.

Google Summer of Code
^^^^^^^^^^^^^^^^^^^^^
Google Summer of Code is a global program where students work with an open source organization
on a 3 month programming project. The core team of Read The Docs proposed some `Project Ideas`_,
one of them was **Refactor & improve our search code**. I_, was keen to get my hand dirty with
Elasticsearch_ and grasped the opportunity to do so by applying
for this project and I got accepted.

I have worked full time for last 3 months to upgrade the whole codebase
to compatable with `Elasticsearch 6.x`_ and also implemented various features
as like:

- `Exact Matching Search`_
- `Case Insensitive Search`_
- `Improved Result Order`_,
- `Zero Downtime Indexing`_

Together with this, I am willing to implement more features like following:

- `Search as You Type and Autocomplete`_
- `Code Search`_ 

All of my search related work can be looked in the `Search Project Board`_.


Background
^^^^^^^^^^
Search is a vital part of any documentation hosting platform as people can get the
information they need. As a documentation hosting platform, same rule applies for
Read The Docs. Because of having a small core team, the search functionality
of Read The Docs has lagged behind for quite a while now. Initially the search code
was voluntarily contributed by `Rob Hudson`_,  `back in 2013`_ and then improved by other
contributors. The time span and continuous technology growing made the search
module got older and it had become outdated. Moreover The search infrastructure was already
vulnerable as Read The Docs were using `Elasticsearch 1.3.x`_ which was already reached its
End of Life in 2016. Therefore, the upgradation of search infrastructure was badly needed.

Sphinx/MkDocs Built in Search vs Read The Docs Search
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Sphinx/MkDocs already have built in search functionality. But the features are very limited.
At Read The Docs, we have felt the limitations and therefore we index the documentations in our
Elasticsearch_ index so that we can provide better search experience like:

- Search across multiple projects
- Advance query syntex
- Search inside subprojects
- Improved search result order
- Public Search API (Documentation pending)

**Currently, we do not index MkDocs documents to** Elasticsearch_,
but `any kind of help is welcome`_.

New Features
^^^^^^^^^^^^
The number of features that can be included in Search is infinity. There are always way to improve.
In the 3 months of full time work, our GSoC student have implemented couple of features including
many bug fixes. Some of the major features are as following:

- `Exact Matching Search`_: Its a highly needed feature for Read The Docs. Now you can search for
  exact word in documentations by having your query inside quotation (`""`). So if you search
  for `"Here is foo"` (with the quotation), you will get all the documentations where the full
  `Here is foo` phrase exist.

- Simple Query String Syntax support: Now you can use `Simple Query String Syntax`_ for
  searching. For example, if you search with `Mozilla +-Firefox`, you will get documentations
  where the `Mozilla` word is present, but `Firefox` word is not present.
  For more information, you can look at `Simple Query String Syntax`_ documentation.

- `Case Insensitive Search`_: The search is now case insensitive. So if you search for `Foo`,
  you will get all the documentations which have one of either `Foo`, `FOO`, `foo` or `fOO`.

- `Improved Result order`_: The result order is improved dramatically. Therefore if you Search
  with `Foo Bar`, you will first see the documentations which have both `Foo Bar`, then
  you will see other documentations which have either `Foo` or `Bar`

- `Auto Removing from Search Index`_: In the past, if any page got removed from documentations,
  the page was still available in documentations. But from now on, the page will be removed
  automatically from the search index as soon as its no longer in the documentation.

- `Zero Downtime Indexing`_: As search is a important part of documentation, there will be no
  downtime while we reindex our Elasticsearch Index. So the search will be much more reliable
  than before.


Performance Improvements
^^^^^^^^^^^^^^^^^^^^^^^^
Performance is always improtant for search. Because of our search was fast enough,
we did not focus to improve the performance. As we have rewritten all the codes with
new search backend engine, we got 4x improved performance as well.

There are 4 kind of search functionality in Read The Docs. The improvements are as following:

- `File Search`_: Search accross all the projects of Read The Docs.

  - Before: 1461 ms
  - After: 200 ms

- `Projects Search`_: Search for projects hosted in Read The Docs.

  - Before: 455 ms
  - After: 162 ms

- `Doc Search API`_: The Public API which is used to perform search in documentation.

  - Before: 746 ms
  - After: 173 ms

- `Project Doc Search`_: Search inside a project documentations from readthedocs.org domain.

  - Before: 750 ms
  - After: 270 ms


Code Improvements
^^^^^^^^^^^^^^^^^
Code quality is very much important in development world, specially in open source.
As I have rewritten the search functionality from scratch, the code quality
is improved in many ways like test coverage and documentations. So its easy for
any contributor to start working on the search functionality

Contributor Wanted
^^^^^^^^^^^^^^^^^^
As Read The Docs is an open source project backed by a small team of developers,
most of them are busy to keep things up and running only. Therefore, its quite
hard for them to take time to implement new features. If you know some bit of
Django or Python and Elasticsearch, you can contribute into the search functionality
of Read The Docs. If you need any support to start contributing, you can knock me or any
member of  Read The Docs team. You can find all of us at `#readthedocs` freenode
IRC channel or `readthedocs gitter`_ channel. I am `safwan` at IRC and `@safwanrahman`
at gitter.

Conclusion
^^^^^^^^^^
To conclude, I must say that the Search improvement in Read The Docs was very much 
necessary and I could improve it in some extent in short amount of time. 
There can be infinity number of ways it can be improved and I believe we can compete
with major search engines in terms of documentation searching.
As I have worked for only 3 months full time, some compelling features are left behind
without implementing like `Search as You Type and Autocomplete`_,
`Code Search`_ functionality. Moreover, proper documentation is needed for the search
architecture. I have tried to write test cases for most of the scenario, but because of
time constrains, a lot of code is out of test coverage. I strongly hope that
we will get the left behind work done within a short amount of time. This can be done
easily if we get more contributors donate their time for improving Read The Docs.
We dont need superhero or coding guru, just need people who understand Python/Django and
Elasticsearch and have some time to write some code for us. You are **SuperHero** to us
if you can lend your time and effort to improve Read The Docs.

.. _Rob Hudson: https://github.com/robhudson
.. _back in 2013: https://github.com/rtfd/readthedocs.org/pull/493
.. _Elasticsearch: https://www.elastic.co/products/elasticsearch
.. _Elasticsearch 1.3.x: https://www.elastic.co/guide/en/elasticsearch/reference/1.3/index.html
.. _Elasticsearch 5.x: https://www.elastic.co/guide/en/elasticsearch/reference/5.4/index.html
.. _Elasticsearch 6.x: https://www.elastic.co/guide/en/elasticsearch/reference/6.3/index.html
.. _Elasticsearch 6.x has major changes: https://www.elastic.co/guide/en/elasticsearch/reference/current/release-notes-6.0.0.html
.. _Project Ideas: https://git.io/fN9GK
.. _I: https://github.com/safwanrahman
.. _Elasticsearch document: https://www.elastic.co/guide/en/elasticsearch/guide/current/document.html
.. _Search Project Board: https://github.com/orgs/rtfd/projects/3
.. _Exact Matching Search: https://github.com/rtfd/readthedocs.org/issues/2457
.. _Case Insensitive Search: https://github.com/rtfd/readthedocs.org/issues/2328
.. _Zero Downtime Indexing: https://github.com/rtfd/readthedocs.org/pull/4368
.. _Simple Query String Syntax: https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-simple-query-string-query.html#_simple_query_string_syntax
.. _Improved Result order: https://github.com/rtfd/readthedocs.org/pull/4292
.. _Search as You Type and Autocomplete: https://github.com/rtfd/readthedocs.org/issues/504
.. _Code Search: https://github.com/rtfd/readthedocs.org/issues/4289
.. _Auto Removing from Search Index: https://github.com/rtfd/readthedocs.org/issues/2013
.. _any kind of help is welcome: https://github.com/rtfd/readthedocs.org/issues/1088
.. _File Search: https://readthedocs.org/search/?q=installation&type=file
.. _Projects Search: https://readthedocs.org/search/?q=kuma&type=project
.. _Doc Search API: https://readthedocs.org/api/v2/docsearch/?q=installation&project=docs&version=latest&language=en
.. _Project Doc Search: https://readthedocs.org/projects/docs/search/?q=installation
.. _readthedocs gitter: https://gitter.im/rtfd/readthedocs.org
.. _core team: https://docs.readthedocs.io/en/latest/team.html#development-team
