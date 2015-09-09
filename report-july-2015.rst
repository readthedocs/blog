.. post:: Sep 9, 2015
   :tags: report
   :author: Anthony

Report - July 2015
==================

August was a hectic month for us. So busy, in fact, we never wrote this update.
We dropped the ball on getting this report out on time, but hope to keep on top
of future updates.

Goals
-----

July was a month of stability fixes, with some substantial changes to our
infrastructure. First, here's an update on some of the goals we had set with
our last monthly update:

Improve Github/Bitbucket integration
    This got pushed to next month, we didn't focus on this as much as we had
    hoped.

Test internal analytics
    We have a basic testbed for internal analytics set up, but haven't gone as
    far as pushing this integration into production. We still need to test
    production load and what the dataset would look like over the course of a
    month.

    This is on hold for the moment.

We also set some additional goals near the beginning of the month:

Finish rolling out a new stack
    Our servers were all reasonably aged and have not been re-provisioned in a
    long while. We set the goal to move all configuration to configuration
    management and be able to reproduce servers in a predictable manner.

    We were able to finish moving all provisioning to configuration management
    and rolled out all new servers, including some new servers.

Improve monitoring
    We have hit a lot of common cases that we should be tracking as part of our
    standard operations notifications. We set the goal to improve our
    notification and debugging capabilities.

    With fresh provisioning, we now also have a programmatic approach towards
    setting up system checks and notifications, and have expanded our reporting
    a great deal.

Update Details
--------------

Ops
~~~

Fresh web servers
    Last month, we rolled out fresh build servers, strictly using configuration
    management to provision servers. This month, we continued by moving web
    server provision to our configuration management and re-rolling all of our
    web servers.

Fresh database servers and migration
    We also rolled new database servers, and took the opportunity to upgrade our
    database's PostgreSQL instance and perform some needed schema changes.

    We decided to perform the migration late one evening, when our then primary
    database server was included in an outage of some Rackspace infrastructure.
    The outage resulted in some extended downtime, and we were not immediately
    able to migrate data from the database server to the fresh instance. The
    outage resolved early in the morning and migration wrapped shortly after.

    The new instance performed better than expected, once we made it live.  The
    fresh instance had more memory and increased bandwidth for disk operations.
    Along with a reindex of a table with slow queries, we noticed significant
    reduction in query times and a great improvement of stability.

Improved monitoring
    We started to catch some edge cases that were not previously monitored and
    improved greatly on our monitoring and graphing.

Dev
~~~

Django 1.8 upgrade
    Our previous version of Django was on the now unsupported 1.6 branch. With
    1.8 released, we felt it was a great chance to finally upgrade our
    dependencies.

Triage process
    We have formalized our `triage process`_ for development. This will guide
    how we make decisions on our issue tracker.

.. _triage process: http://docs.readthedocs.org/en/latest/contribute.html#triaging-tickets

Linting
    Linting has not been performed on the codebase for a long while. We felt
    this was important to get back to in order to ensure code quality.

Stable version improvements
    There has been some buggy behavior behind the stable version detection. We
    worked here to clean up some of the broken behavior.

Fix slugging on versions
    There have been a number of error cases that have surfaced around version
    slugging recently. This works to fix some logic errors on edge cases.


For more information on our development orchestration, visit or subscribe to our
`public Trello board`_.

.. _`public Trello board`: https://trello.com/b/tF04aNrT/read-the-docs-public

Issues
------

In the month of July:

 * Read the Docs saw `80 new issues`_
 * 50 of those issues `have been closed`_
 * Additionally, `35 outstanding issues`_ were closed out

.. _`80 new issues`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A2015-07-01..2015-07-31+type%3Aissue
.. _`have been closed`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A2015-07-01..2015-07-31+type%3Aissue+state%3Aclosed
.. _`35 outstanding issues`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A%3C2015-07-01+type%3Aissue+state%3Aclosed+closed%3A2015-07-01..2015-07-31

Feel free to raise any questions you have about any of these changes on our
`issue tracker`_, or on our Freenode IRC channel, #readthedocs.

.. _`issue tracker`: https://github.com/rtfd/readthedocs.org/issues

Goals for Next Month
--------------------

Improve Github/Bitbucket integration
    We have pushed this up to next month, we still need to address some failures
    as part of Github/Bitbucket integration.

Better Sphinx experience for authoring
    We can streamline a lot of the experience around using Sphinx, and at the
    same time, make more reproduceable builds, locally, for authors. This would
    involve mimicking more of what we preform in our build backend for local
    authoring.

More code cleanup
    We started some linting efforts to bring code quality up, we will continue
    deeper and more thorough linting efforts.

More features to user gold subscription
    We would like to have more users on a recurring subscription, which is a
    great step towards sustainability. We should be surfacing features and
    reminding users to donate if they are using some of those features.
