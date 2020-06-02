.. post:: May 14, 2020
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

* 465 Million Page Views (from 400M)
* 120 Million Unique Visitors (from 77M)

.. From Google Analytics

These numbers are not completely accurate, since we :doc:`implemented Do Not Track support </do-not-track>` last year, our analytics pageview figures understate our actual traffic.
We estimate that around 6% of users are not counted here.
We also don't count all the users who block Google Analytics with a browser extension.

Site Stats
----------

The stats, in total numbers:

* 200,000 projects (from 100k)
* 400,000 users (from 150k)
* 10,188,182 builds (new this year)

We have been battling spam quite heavily again this year,
so these numbers are a bit skewed.
We do notice a uptick in usage across the site,
both in terms of support and traffic.

.. Project.objects.count()
.. User.objects.count()
.. Build.objects.filter(date__year__lte=2019).first().pk

Community
---------

This year, we had:

* 21 `people`_ who committed code to the main repository (from 28)
* 4793 `commits`_ (from 3774)
* 609 `issues`_ - 80 open, 529 closed (from 797)

We have continued to have a similar team working on the project this year,
but have actually made more commits.
We moved our support queue from issues to email,
which likely accounts for the lower issue count.
We're quite happy with our closed issue stats this year,
which are much better than previous years.

.. git rev-list --count --all --after="2018-12-31" --before="2020-01-01"

.. _people: https://github.com/rtfd/readthedocs.org/graphs/contributors?from=2019-01-01&to=2019-12-31&type=c
.. _commits: https://github.com/rtfd/readthedocs.org/commits/master
.. _issues: https://github.com/readthedocs/readthedocs.org/issues?q=is%3Aissue+created%3A2019-01-01..2019-12-31+

Funding
-------

* $275,000 in revenue from readthedocs.org (from 294,000)
* $249,000 from advertising (from $278,000)
* $26,600 from Gold users (from $16,000)
* We have additional revenue from our commercial offering at readthedocs.com, but aren't including that in our community funding overview

Our advertising has been pretty steady for 2019.
The small drop in the year-over-year comparison we account to the fact that ad blockers happened halfway through 2018,
meaning that the comparison is 15% lower in terms of our total traffic.

We continue to be hosted by Azure_,
and we're using a lot of their nicer feature to keep our costs down.
You can find some posts on our blog about this.

.. _Azure: https://azure.microsoft.com/en-us/

Conclusion
----------

We continue to keep working to improve the documentation ecosystem in the software industry.
We're excited about a number of new features that we're working on this year,
and expect to continue to be a resource you can depend on for a long time to come :)
