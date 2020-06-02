.. post:: Jan 8, 2019
   :tags: stats, year-in-review

Read the Docs 2018 Stats
========================

2018 was another good year for `Read the Docs`_.
We've settled into a sustainability model that is working for us,
and have a team of 5 folks working full-time on the project.

Here are our stats for the past year,
which we've published for the past 6 years.
This is part of our effort to be transparent in our organization,
as well as our source code.

.. note:: 

	You can always see our stats for the last `30 days`_. 

	Our posts from 2013_, 2014_, 2015_, 2016_, and 2017_ are also available.

.. _Read the Docs: https://readthedocs.org/
.. _30 days: http://www.seethestats.com/site/readthedocs.org
.. _2013: https://blog.readthedocs.com/read-the-docs-2013-stats/
.. _2014: https://blog.readthedocs.com/read-the-docs-2014-stats/
.. _2015: https://blog.readthedocs.com/read-the-docs-2015-stats/
.. _2016: https://blog.readthedocs.com/read-the-docs-2016-stats/
.. _2017: https://blog.readthedocs.com/read-the-docs-2017-stats/


Page Views
----------

Our stats:

* 400 Million Page Views (up from 338M, 18%)
* 77 Million Unique Visitors (up from 75M, 3%)

.. From Google Analytics

These numbers are not completely accurate, since we :doc:`implemented Do Not Track support </do-not-track>` in May, our analytics pageview figures understate our actual traffic.
We estimate that around 6% of users are not counted here.
We also don't count all the users who block Google Analytics with a browser extension.

Site Stats
----------

The stats, in total numbers:

* 100,000 projects (up from 77k, 30%)
* 155,000 users (up from 103k, 50%)

We have been battling spam quite heavily again this year,
so these numbers are a bit skewed.

.. Project.objects.count()
.. User.objects.count()

Community
---------

This year, we had:

* 28 `people`_ who committed code to the main repository (up from 23, 22%)
* 3774 `commits`_ (up from 1058, 257%)
* 797 `issues`_ - 189 open, 608 closed (up from 513, 55%)

You can see the number of commits and issues has gone up quite a bit.
This is largely because of the additional staffing we have had on the project,
allowing us to be more active to both our users and to release more features.

.. git rev-list --count --all --after="2017-12-31" --before="2019-01-01"

.. _people: https://github.com/rtfd/readthedocs.org/graphs/contributors?from=2018-01-01&to=2018-12-31&type=c
.. _commits: https://github.com/rtfd/readthedocs.org/commits/master
.. _issues: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=is%3Aissue++created%3A2018-01-01..2019-01-01+

Funding
-------

* $294,000 in revenue from readthedocs.org (up from $218,000, 35%)
* $278,000 from advertising (up 59%)
* $16,000 from Gold users (up 16%)
* We have additional revenue from our commercial offering at readthedocs.com, but aren't including that in our community funding overview

The biggest impact to our revenue this year was :doc:`our ads being blocked </ads-and-adblocking>`.
This happened in May,
and caused an initial 32% reduction in our ad revenue.
We were :doc:`added to the Acceptable Ads </ad-blocker-update>` list later in the month,
which regained around half of our revenue.
So for the second half of the year,
our ad revenue was down about 15%.

We are also exploring sharing revenue with our documentation authors.
There are currently 3 projects enrolled in a revenue share,
and we're hoping to expand that in 2019 to better support open source projects.

The project is now on firm financial footing.
We have a cash reserve that will allow us to pay all of our staff for more than 3 months in the event of a loss of revenue,
which allows us to be more flexible with our revenue going forward. 
This funding allowed us to expand from 4 to 5 full-time folks working on the project.

We also moved hosting to Azure_ this year in August from Rackspace_,
who both have sponsored our hosting.

.. _Rackspace: http://rackspace.com/
.. _Azure: https://azure.microsoft.com/en-us/

Conclusion
----------

This year we've continued to invest in our ethical advertising approach,
growing our team by one member and building lots of new features.
It feels like the project is progressing quite well,
and we're committing way more code and dealing with a much larger number of user issues.

It feels like success to be able to properly support our community by improving the product,
while creating a business model that we can be proud of.
