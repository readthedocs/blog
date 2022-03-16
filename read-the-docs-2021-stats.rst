.. post:: Mar 17, 2022
   :tags: stats, year-in-review

Read the Docs 2021 Stats
========================

2021 continued in the realm of being a tough year.
That said,
Read the Docs had a lot of good things happen this year.

We did a majority of the owrk on our :doc:`CZI grant </czi-grant-announcement>`,
grew our team from 5 to 8,
and continued to grow our `EthicalAds network`_.
It's been a year of continued growth,
and we hope to continue that into 2022.

As we have for the past 8 years (!!),
we are proud to share our 2021 stats post.

.. _EthicalAds network: https://www.ethicalads.io/

.. note::

	You can always see our stats for the last `30 days`_.

	Our posts from 2013_, 2014_, 2015_, 2016_, 2017_, 2018_, 2019_, and 2020_ are also available.

.. _Read the Docs: https://readthedocs.org/
.. _30 days: http://www.seethestats.com/site/readthedocs.org
.. _2013: https://blog.readthedocs.com/read-the-docs-2013-stats/
.. _2014: https://blog.readthedocs.com/read-the-docs-2014-stats/
.. _2015: https://blog.readthedocs.com/read-the-docs-2015-stats/
.. _2016: https://blog.readthedocs.com/read-the-docs-2016-stats/
.. _2017: https://blog.readthedocs.com/read-the-docs-2017-stats/
.. _2018: https://blog.readthedocs.com/read-the-docs-2018-stats/
.. _2019: https://blog.readthedocs.com/read-the-docs-2019-stats/
.. _2020: https://blog.readthedocs.com/read-the-docs-2020-stats/


Page Views
----------

Our stats:

* 700 Million Page Views (from 580 million)
* 196 Million Unique Visitors (from 156 million)

.. From Google Analytics

These numbers are not completely accurate, since we :doc:`implemented Do Not Track support </do-not-track>` our analytics pageview figures understate our actual traffic.
We estimate that around 6% of users are not counted here.
We also don't count all the users who block Google Analytics with a browser extension.

Of note, we host a `major documentation site <http://faq-login-unico.servicos.gov.br/en/latest/>`_ for the Brazilian government,
which is our largest site by a wide margin,
but they are in both years data.

Site Stats
----------

The stats, in total numbers:

* 45,849 new projects (from 40,000)
* 56,760 new users (from 30,000)
* 2,831,885 builds (from 2,480,063)

We have been battling spam quite heavily again this year,
so these numbers are a bit skewed.
We have worked to improve our spam detection though,
and are in a much better place with spam this year.

.. Project.objects.filter(pub_date__year=2021).count()
.. User.objects.filter(date_joined__year=2021).count()
.. Build.objects.filter(date__year=2021).count()

Community
---------

This year, we had:

* 14 `people`_ who committed code to the main repository (from 14)
* 2126 `commits`_ (from 3636)
* 376 `issues`_ - 88 open, 288 closed (from 532)

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

* TODO advertising (from $234,000)
* TODO Gold users and donations (from $30,000)
* 8 paid staff (from 5)
* We have additional revenue from our commercial offering at readthedocs.com, but aren't including that in our community funding overview

We are excited to continue to grow our advertising business,
and expand it to the larger community.
We are also seeing continued growth of our paid product at https://readthedocs.com,
which is allowing us to fund further growth of the Read the Docs codebase for all our users.

.. _EthicalAds: https://www.ethicalads.io/


Conclusion
----------

We continue to work to improve Read the Docs for our users.
We're excited for the growth we expect in 2022,
and hope that you'll join us for the next chapter of our story.

The Read the Docs Team
