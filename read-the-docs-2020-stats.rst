.. post:: Mar 17, 2021
   :tags: stats, year-in-review

Read the Docs 2020 Stats
========================

2020 was a rough year for everyone,
including our team.
We managed to make it through,
and continue to have 5 folks working full-time to make Read the Docs better for you.

We are going into 2021 with a :doc:`new grant </czi-grant-announcement>`,
which will require us to do some :doc:`hiring </jobs>`.
We also launched our `EthicalAds network`_,
which is bringing our approach to sustainability to the tech community as a whole.

As we have for the past 7 years,
we are proud to share our 2020 stats post.

.. _EthicalAds network: https://www.ethicalads.io/

.. note::

	You can always see our stats for the last `30 days`_.

	Our posts from 2013_, 2014_, 2015_, 2016_, 2017_, 2018_, and 2019_ are also available.

.. _Read the Docs: https://readthedocs.org/
.. _30 days: http://www.seethestats.com/site/readthedocs.org
.. _2013: https://blog.readthedocs.com/read-the-docs-2013-stats/
.. _2014: https://blog.readthedocs.com/read-the-docs-2014-stats/
.. _2015: https://blog.readthedocs.com/read-the-docs-2015-stats/
.. _2016: https://blog.readthedocs.com/read-the-docs-2016-stats/
.. _2017: https://blog.readthedocs.com/read-the-docs-2017-stats/
.. _2018: https://blog.readthedocs.com/read-the-docs-2018-stats/
.. _2019: https://blog.readthedocs.com/read-the-docs-2019-stats/


Page Views
----------

Our stats:

* 580 Million Page Views (from 465 million)
* 156 Million Unique Visitors (from 120 million)

.. From Google Analytics

These numbers are not completely accurate, since we :doc:`implemented Do Not Track support </do-not-track>` our analytics pageview figures understate our actual traffic.
We estimate that around 6% of users are not counted here.
We also don't count all the users who block Google Analytics with a browser extension.

Site Stats
----------

The stats, in total numbers:

* 240,000 projects (from 200,000)
* 430,000 users (from 400,000)
* 2,480,063 builds (from 10 million total last year)

We have been battling spam quite heavily again this year,
so these numbers are a bit skewed.
We do notice a uptick in usage across the site,
both in terms of support and traffic.

.. Project.objects.count()
.. User.objects.count()
.. Build.objects.filter(date__year__lte=2021).first().pk - Build.objects.filter(date__year__lte=2020).first().pk

Community
---------

This year, we had:

* 14 `people`_ who committed code to the main repository (from 21)
* 3636 `commits`_ (from 4793)
* 532 `issues`_ - 104 open, 428 closed (from 609)

We have been working to move user support issues to email from GitHub,
which likely addresses the reduction in ticket numbers.
We are also working to expand our ecosystem of projects,
so the commits to the main repository are down.
We expect across our theme, extensions, and other projects commits are up this year,
and we're appreciative of all the work people contribute.


.. git rev-list --count --all --after="2019-12-31" --before="2021-01-01"

.. _people: https://github.com/rtfd/readthedocs.org/graphs/contributors?from=2020-01-01&to=2020-12-31&type=c
.. _commits: https://github.com/rtfd/readthedocs.org/commits/master
.. _issues: https://github.com/readthedocs/readthedocs.org/issues?q=is%3Aissue+created%3A2020-01-01..2020-12-31+

Funding
-------

* $234,000 advertising (from $249,000)
* $30,000 Gold users and donations (from $26,600)
* 5 paid staff (same as last year)
* We have additional revenue from our commercial offering at readthedocs.com, but aren't including that in our community funding overview

With the launch of `EthicalAds`_, we are excited to continue to grow our advertising business,
and expand it to the larger community.
We are also seeing continued growth of our paid product at https://readthedocs.com,
which is allowing us to fund further growth of the Read the Docs codebase for all our users.

.. _EthicalAds: https://www.ethicalads.io/


Conclusion
----------

We continue to work to improve Read the Docs for our users.
We're excited for the growth we expect in 2021,
and hope that you'll join us for the next chapter of our story.

The Read the Docs Team
