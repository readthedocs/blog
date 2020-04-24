.. post:: Apr 28, 2020
   :tags: stats, year-in-review

Read the Docs 2019 Stats
========================

2019 was another good year for `Read the Docs`_.
We continue to have a team of 5 folks working on the project,
and we've rolled out a number of new features for the year.

Here are our stats for the past year,
which we've published since 2013.
This is part of our effort to be transparent in our organization,
as well as our source code.

.. note:: 

	You can always see our stats for the last `30 days`_. 

	Our posts from 2013_, 2014_, 2015_, 2016_, 2017_, and 2018_ are also available.

.. _Read the Docs: https://readthedocs.org/
.. _30 days: http://www.seethestats.com/site/readthedocs.org
.. _2013: https://blog.readthedocs.com/read-the-docs-2013-stats/
.. _2014: https://blog.readthedocs.com/read-the-docs-2014-stats/
.. _2015: https://blog.readthedocs.com/read-the-docs-2015-stats/
.. _2016: https://blog.readthedocs.com/read-the-docs-2016-stats/
.. _2017: https://blog.readthedocs.com/read-the-docs-2017-stats/
.. _2018: https://blog.readthedocs.com/read-the-docs-2018-stats/


Page Views
----------

Our stats:

* 465 Million Page Views (up from 400M)
* 120 Million Unique Visitors (up from 77M)

.. From Google Analytics

These numbers are not completely accurate, since we :doc:`implemented Do Not Track support </do-not-track>` last year, our analytics pageview figures understate our actual traffic.
We estimate that around 6% of users are not counted here.
We also don't count all the users who block Google Analytics with a browser extension.

Site Stats
----------

The stats, in total numbers:

* 200,000 projects (up from 100k)
* 400,000 users (up from 150k)

We have been battling spam quite heavily again this year,
so these numbers are a bit skewed.

.. Project.objects.count()
.. User.objects.count()

Community
---------

This year, we had:

* 21 `people`_ who committed code to the main repository (down from 28)
* 4793 `commits`_ (up from 3774)
* 609 `issues`_ - 80 open, 529 closed (down from 797)

We have continued to have a similar team working on the project.
In particular I'm happy with our closed issue stats this year,
which are much better than previousy years

.. git rev-list --count --all --after="2018-12-31" --before="2020-01-01"

.. _people: https://github.com/rtfd/readthedocs.org/graphs/contributors?from=2019-01-01&to=2019-12-31&type=c
.. _commits: https://github.com/rtfd/readthedocs.org/commits/master
.. _issues: https://github.com/readthedocs/readthedocs.org/issues?q=is%3Aissue+created%3A2019-01-01..2019-12-31+

Funding
-------

* $TODO in revenue from readthedocs.org (from 294,000)
* $TODO from advertising (from $278,000)
* $TODO from Gold users (from $16,000)
* We have additional revenue from our commercial offering at readthedocs.com, but aren't including that in our community funding overview


We continue to be hosted by Azure_,
and we're using a lot of their nicer feature to keep our costs down.
You can find some posts on our blog about this.

.. _Azure: https://azure.microsoft.com/en-us/

Conclusion
----------
