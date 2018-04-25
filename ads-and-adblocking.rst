.. post:: April 10, 2018
   :tags: advertising, privacy, sustainability, business, adblock
   :author: David
   :location: SAN

.. TODO: update date

Ads and Ad blockers at Read the Docs
====================================

Last week, we talked about how :doc:`ethical advertising works <ethical-advertising-works>`.
Read the Docs has a number of sources of revenue from our `paid product`_
to donations but by far the largest source of revenue comes from advertising.
Our premium audience of professional and amateur software developers engaged
in reading about the software they use has proved to be quite valuable to
advertisers. Furthermore, we have been able to build our advertising model
while **respecting user privacy** which our audience frequently and repeatedly
tells us is very important to them. We declared we:

* Never let advertisers run scripts on our site and always
  host ad images ourselves. [#f1]_
* Never provide data dumps of personal data to advertisers.
* Only target advertising based on general geography [#f2]_ and the details
  of the page being visited not a trove of behavioral data about visitors.

Read the Docs `continues to grow <read-the-docs-2017-stats>`_ by every metric
despite not taking the all too typical route of cashing in
without considering the consequences on users.
With all this success, it was only a matter of time before we attracted
the attention of ad blockers.

.. _paid product: https://readthedocs.com/pricing/


All about ad blockers
---------------------

Ad blockers fulfill a legitimate need to mitigate the
`significant downsides of advertising`_ from tracking across the internet,
security implications of third-party code,
and impacting the UX and performance of sites.
Read the Docs runs a one-site ad network but most of our developers run
ad blockers. That should tell you what you need to know about the ad industry.
That's why we built the ad network we wanted to exist with
no tracking and no behavioral targeting.

According to a `2017 report from PageFair`_ (pdf), a company that specializes
in quantifying ad blocking, 11% of global web users run an ad blocker.
Considering that Read the Docs' core audience is tech-savvy, privacy-conscious
developers, it should be no surprise that our number is higher.

Most ad blockers work by subscribing users to "filter lists" that have rules
to block ads or other content based on CSS selectors or URL patterns.
The largest and most popular of these filter lists is called the `EasyList`_.
Read the Docs' success in advertising led us to get added to the EasyList.

.. _significant downsides of advertising: https://docs.readthedocs.io/en/latest/ethical-advertising.html#ethical-info
.. _2017 report from PageFair: https://pagefair.com/downloads/2017/01/PageFair-2017-Adblock-Report.pdf
.. _EasyList: https://easylist.to/


Ad blocker fallout
------------------

.. figure:: img/2018-readthedocs-adblocker-fallout.png
   :alt: Effect of ad blocking on Read the Docs ad views
   :width: 100%

Getting added to the EasyList had a significant and immediate impact on the
bottom line at Read the Docs. Right around April 1,
**32% of our ad views simply vanished**.
At first, we thought we had done something horribly wrong but then we
discovered that this was due entirely to ad blocking.
Our actual traffic wasn't down at all.
Users' browsers were simply downloading the updated EasyList which blocked ads
on Read the Docs.
In terms of ad viewership, weekdays
-- our busiest days and the peaks in the graph -- became more like
weekends and weekends fell off a cliff.
We had always guessed what percentage of our user base ran ad blockers.
Now we know. We knew this day would come but we had hoped it was a ways off
considering we weren't part of a large ad network.

This directly affected our operations and staff. Our operating costs
didn't go down in any significant way, but revenue sure did. This meant that
we had to cut some costs where we could and slow down some hiring plans.
While Read the Docs is not a non-profit company, all the revenue is
reinvested into the project itself, paying maintainers, and other places
in the open source ecosystem. The situation is not dire by any means,
but it was certainly disappointing that we ended up on the same list with
popup advertisers who couldn't care less about privacy.


What are we doing about it
--------------------------

It will be an uphill battle to get back to where we were in terms of revenue
and sustaining Read the Docs, but I thought I would highlight a few things
we are working on:

.. TODO: update if/when we get on the list...

* We applied to the `acceptable ads`_ list, a filter list enabled on many
  ad blockers by default that enables some unobtrusive advertising. We are
  very hopeful here but it does take quite a bit longer to get on this list
  than it does to get blocked.
* Nagging users into whitelisting Read the Docs. We are envisioning more
  of a polite nag in a similar vein to `jsfiddle`_ rather than an
  "adblock wall" which prevents usage of Read the Docs until it's whitelisted.
* Blogging and raising awareness of how ad blocking affects us and other
  open source projects.

While we could simply change our CSS and ad API to avoid blocking
since we host our ads ourselves,  we decided not to engage
in a cat and mouse game since this work would not benefit users.

Advertising funds much of the web and many people recognize
that while there are plenty of bad actors in the ad industry
-- think pop-under ad networks or ads that navigate your browser for you --
some advertising is necessary to power the web we know and love especially
when it comes to open source software which has
`unique funding challenges`_.

.. _acceptable ads: https://acceptableads.com/
.. _jsfiddle: https://jsfiddle.net/
.. _unique funding challenges: https://www.fordfoundation.org/library/reports-and-studies/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/


Open source advertising whitelist
---------------------------------

At Read the Docs, we also discovered that we are not the only open source
project that got our advertising blocked by ad blockers.
Many open source projects that fund themselves
through advertising get blocked and some of them don't have the resources
to navigate the acceptable ads program or understand the inner workings
of ad blockers.
Likewise, some web users may not want to allow all acceptable ads which
includes many ads from the big networks but we are hoping they would be
willing to accept ads that benefit their community of software developers.

We are launching a **new initiative** to
`whitelist advertising that benefits open source software`_. We encourage
you to subscribe to the this list and support open source. If you run an
open source project affected by ad blockers, we would love to help
you too.

.. _whitelist advertising that benefits open source software: https://ads-for-open-source.readthedocs.io

.. admonition:: Advertisers

    If you are an advertiser interested in reaching a 100% developer
    audience who cares deeply about privacy,
    we would love to `hear from you`_ too.

    .. _hear from you: https://readthedocs.org/sustainability/advertising/#advertise-cta


.. FOOTNOTES

.. [#f1] Letting advertisers host images can result in long-lived tracker
         cookies and leaking of IP addresses. Users don't want that.
.. [#f2] Currently this means a country but we might expand this to US states.
         You can read more about ad targeting in our `advertising FAQ`_.

.. _advertising FAQ: https://readthedocs.org/sustainability/advertising/faq/
