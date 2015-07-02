Report - June 2015
==================

With the `Write the Docs`_ conference wrapped up in May, we shifted our focus
back to Read the Docs for the remainder of May and June. Following our post `on
contract positions available with Read the Docs`_, we hired two contractors to
work with us and focus on support and stability for readthedocs.org. `Gregor
Müllegger`_ will be working on support and development, and `Andrew Kreps`_ has
helped us on building and improving our operations infrastructure.

.. _`Write the Docs`: http://writethedocs.org
.. _`Gregor Müllegger`: https://github.com/gregmuellegger
.. _`Andrew Kreps`: https://github.com/onewheelskyward

Read the Docs had the following major updates in June:

 * Elastic Search support was upgraded and our search cluster is now hosted on
   `Found`_.
 * We did a fresh provision of our build cluster. Previously, there were slight
   disparities between the servers, which surfaced some issues during builds.
 * Output formats such as PDF and ePub are now configurable, and won't default
   to building. This should reduce build contention significantly.
 * We started to address outstanding issues with stable version detection and
   version name handling.
 * Static assets were migrated to use a CDN, provided by `MaxCDN`_.
 * In order to move away from third party tracking, we have spun up services for
   internal tracking. We plan on testing internal tracking in the coming months.
 * We have shifted our focus to greatly improving the Read the Docs
   infrastructure, including monitoring and notifications, as well as server
   environment consistency.

For more information on our development orchestration, visit or subscribe to our
`public Trello board`_.

.. _`Found`: http://found.no
.. _`MaxCDN`: http://maxcdn.com
.. _`public Trello board`: https://trello.com/b/tF04aNrT/read-the-docs-public

Issues
------

We have started to formalize on a ticket triage process and have more focus on
performing project management in the open. This is a very welcome change to our
existing workflow and hope to continue improving on it.

In the month of June:

 * Read the Docs saw `50 new issues`_ in the month of June
 * 26 of those issues `have been closed`_
 * `The remaining 24`_ have been triaged but remain unresolved
 * Additionally, `19 outstanding issues`_ were closed out

.. _`50 new issues`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A2015-06-01..2015-06-30+type%3Aissue
.. _`have been closed`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A2015-06-01..2015-06-30+type%3Aissue+state%3Aclosed
.. _`The remaining 24`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A2015-06-01..2015-06-30+type%3Aissue+state%3Aopen
.. _`19 outstanding issues`: https://github.com/rtfd/readthedocs.org/issues?utf8=%E2%9C%93&q=created%3A%3C2015-06-01+type%3Aissue+state%3Aclosed+closed%3A2015-06-01..2015-06-30

Next Month
----------

Once work is wrapped up on version detection cleanup, we hope to start
addressing bugginess with Github/Bitbucket integration and user experience
issues around deleting unwanted content from Read the Docs.

We will also be testing internal analytics in the coming months. Our stance is
that user data, for both our users and for readers of hosted documentation,
should not be handed over to third party services like Google Analytics. We hope
to replace external analytics with an internally hosted service, so that your
data can remain private.

Feel free to raise any questions you have about any of these changes on our
`issue tracker`_, or on our Freenode IRC channel, #readthedocs.

.. _`issue tracker`: https://github.com/rtfd/readthedocs.org/issues
