.. post:: August 14, 2018
   :tags: gsoc, search, feature
   :author: Safwan
   :location: DHA

Search Improvements
====================

Background
^^^^^^^^^^
Search is a vital part of any documentation hosting platform as people can get the
information they need. As a documentation hosting platform, same rule applies for
Read The Docs. Because of having a small core team, the search functionality
of Read The Docs has lagged behind for quite a while now. Initially the search code
was volunteerly contributed by `Rob Hudson`_,  `back in 2013`_ and then improved by other 
contributors. The time span and continuous technology growing made the search
module got older and it had become outdated. The search infrastructure was already vulnerable
as we were using `Elasticsearch 1.3.x`_ which was already reached its End of Life in 2016.
Therefore, the upgradation of search infrastructure was badly needed.

Google Summer of Code
~~~~~~~~~~~~~~~~~~~~~
Google Summer of Code is a global program where students work with an open source organization
on a 3 month programming project. Earlier this year, Read The Docs applied to become a Mentor
Organization and was selected. The core team of Read The Docs proposed some `Project Ideas`_,
one of them was **Refactor & improve our search code**. Our contributor (me) `Safwan Rahman`_, an undergraduate university student and open source contributor from Bangladesh was keen
to get his hand dirty with `Elasticsearch`_ and grasped the opportunity to do so by applying for this project and got accepted.

Initially the plan was to upgrade the search infrastructure from `Elasticsearch 1.3.x`_
to `Elasticsearch 5.x`_, but later Safwan_ proposed the core team to upgrade to
`Elasticsearch 6.x`_. The decision was quite challenging because `Elasticsearch 6.x has major changes`_ that are not compatable with exisiting Read The Docs architecture. But the GSoC
student Safwan_ and the core team was ambitious to rewrite the exisiting architecture from
scratch to make it compatable with `Elasticsearch 6.x`_.

As decided by the whole team, Safwan_ has worked full time for last 3 months to upgrade the
whole codebase to compatable with `Elasticsearch 6.x`_ and also fixing the issue filled by
the users. Most of the issues were about new features of the search functionality. All of his
search related work can be checked in the `Search Project Board`_.

.. _Rob Hudson: https://github.com/robhudson
.. _back in 2013: https://github.com/rtfd/readthedocs.org/pull/493
.. _Elasticsearch: https://www.elastic.co/products/elasticsearch
.. _Elasticsearch 1.3.x: https://www.elastic.co/guide/en/elasticsearch/reference/1.3/index.html
.. _Elasticsearch 5.x: https://www.elastic.co/guide/en/elasticsearch/reference/5.4/index.html
.. _Elasticsearch 6.x: https://www.elastic.co/guide/en/elasticsearch/reference/6.3/index.html
.. _Elasticsearch 6.x has major changes: https://www.elastic.co/guide/en/elasticsearch/reference/current/release-notes-6.0.0.html
.. _Project Ideas: https://git.io/fN9GK
.. _Safwan Rahman: https://github.com/safwanrahman
.. _Safwan: https://github.com/safwanrahman
.. _Elasticsearch document: https://www.elastic.co/guide/en/elasticsearch/guide/current/document.html
.. _Search Project Board: https://github.com/orgs/rtfd/projects/3
