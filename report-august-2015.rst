.. post:: Sep 9, 2015
   :tags: report
   :author: Anthony

Report - August 2015
====================

August was a busy month for us. `Write the Docs Europe`_ was at the end of the
month, and our focus has been on getting `readthedocs.com`_ into a
public beta state. We're nearing the end of the 3 month period that we budgeted
for as part of our fundraiser and have a few more tasks to push out.

.. _Write the Docs Europe: http://www.writethedocs.org/conf/eu/2015/
.. _readthedocs.com: https://readthedocs.com

Goals
-----

First, an update of the goals we set for this month:

Improve Github/Bitbucket integration
    We fixed a very common bug caused by the way implemented syncing to the
    Github API. There are still some user experience issues we would like to
    address.

Better Sphinx experience for authoring
    We started to refactor parts of our build backend and discussed what the
    optimal tool for authors would be. We don't have a clear sense of where to
    split up our build backend code and what is extraneous to authors yet,
    however.

More code cleanup
    Linting cleanup progressed, and we are on to discussing stricter linting
    efforts.

More features to user gold subscription
    We have added the ability to "bless" projects with a gold subscription, but
    are still working on the user experience behind reminding users to donate
    via gold subscriptions, nor are we explaining gold to users yet.

Update Details
--------------

Build backend refactor
    The builder backend code was refactored and now all build commands executed
    are tracked and associated with builds. This surfaced a number of hidden
    commands and a few failure conditions that were being disregarded.

    This also removes the confusing magic PDF build that gets triggered from a
    normal build object.

Build output page
    With the build refactor tracking all commands separately, we can now show
    output of all the commands executed. Before this output was split into
    output and error output streams, and it wasn't always easy to distinguish
    failures. The build output page will now also live update through the API as
    changes become available.

Improved Github Syncing
    Our initial attempt at Github integration updated from the Github API
    in-process, which could result in a timeout when the API didn't return quick
    enough. Syncing against the API was moved to our task queue, with an API to
    monitor changes to the task.

Started work on more automated build toolchain
    We have plans to make the process for building Sphinx documentation more
    automated for authors. We started laying out plans for what that tool would
    look like and how it would function.

For more information on our development orchestration, visit or subscribe to our
`public Trello board`_.

.. _`public Trello board`: https://trello.com/b/tF04aNrT/read-the-docs-public

Issues
------

In the month of August:

 * Read the Docs saw `55 new issues`_
 * 36 of those issues `have been closed`_
 * Additionally, `59 outstanding issues`_ were closed out

.. _`55 new issues`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A2015-08-01..2015-08-31+type%3Aissue
.. _`have been closed`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A2015-08-01..2015-08-31+type%3Aissue+state%3Aclosed
.. _`59 outstanding issues`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A%3C2015-08-01+type%3Aissue+state%3Aclosed+closed%3A2015-08-01..2015-08-31

Feel free to raise any questions you have about any of these changes on our
`issue tracker`_, or on our Freenode IRC channel, #readthedocs.

.. _`issue tracker`: https://github.com/rtfd/readthedocs.org/issues

Goals for Next Month
--------------------

Improve gold subscriptions more
    With the fundraiser funds nearly allocated, we need to begin budgeting for
    the next few months, and will need to start bringing in income. We want to
    improve the user experience around donating, as well as present more
    reminders to donate to active users.

Increase income for the community site
    With better user experience around donating, we hope to launch another
    effort to get more users and companies to donate.

Improve import user experience
    There are still some gritty parts to the import process that should be
    streamlined. Some of the major Github bugs have been squashed, but a larger
    UX improvement is still required.
