.. post:: Sep 9, 2015
   :tags: report
   :author: Anthony

State of the Docs
=================

August has historical significance for Read the Docs, so it seemed fitting to
wrap up August by taking a moment to step back and reflect on what we've done in
the last year.

*What makes August so significant for us?*

For starters, this August saw the `5th birthday of Read the Docs <bday_>`_!
We're still humbled by the project's success, and the important role it
continues to play for old and new users alike.

This growth was becoming difficult to manage without focused support given back
to the community. Though the project has always had core maintainers, for Read
the Docs to continue growing as a community resource, we knew it required
dedicated attention.

This is the reason why, in August of last year, Eric and I set out to create a
company around Read the Docs -- another significant bookmark in Read the Docs'
history. We planned to build the company to fund the ongoing support efforts of
the community site and to help accelerate its growth. At this time last year, we
had just formed Read the Docs, Inc, we were fresh into the `PIE accelerator
program <pie_>`_, and we were planning how to bring our documentation values to
companies that weren't open source.

.. _bday: http://ericholscher.com/blog/2010/aug/16/announcing-read-docs/
.. _pie: http://piepdx.com


The last year
-------------

Our primary goal has always been to drive the development of our community site,
with hopes that it would one day be self-sustaining. We made a number of
decisions and changes to work towards this goal in the last year:

Treat the community site as a separate entity
    In order to be independently sustainable, the community site needs income of
    its own. The service is large enough now that dedicated staff is a
    necessity. There needs to be someone to drive development, handle support
    requests, and be accountable for keeping everything running.

    Currently, all money coming into Read the Docs is treated as income into the
    business. We do track income to the community site separately, so we can
    budget for the community site separately from running the rest of the
    business.

    We aren't yet to the point where this split is critical. There are no
    employees of the business yet, and we are only able to pay ourselves for a
    small portion of the work we perform for the community site.

    We will need to track this explicitly as we grow however, as the community
    site will need to rely on donations for the foreseeable future. Those
    donations should not go towards developing the for-profit side directly.
    Development of the community site will still be a primary function of income
    into the for-profit side.

    Eventually, the community site could be structured completely separate, to
    provide a more explicit split.  It could probably be structured as a 501c,
    This doesn't make financial sense yet.

Our support fundraiser
    In an effort to fund development and maintenance on the community site, we
    decided to call on our community for financial support back in June.  This
    was the first time we have asked the community for contributions.  Our goal
    was to fund at least a portion of the time spent developing and supporting
    the community site.

    Thanks to all the contributors from our community, we raised our goal of
    $24,000, and were able to fund the time of multiple engineers working
    steadily on Read the Docs for the last few months.

    We already outlined our costs and our plans behind our June fundraiser in a
    previous post. We will be following up the last few months of work with an
    overall review of the fundraiser and the work we performed in the coming
    weeks.

Triaging
    Hopefully, our support responsiveness has been more apparent.  One hurdle in
    bringing on more engineers, and engaging the community more, was the lack of
    formal ticketing and open decision making.  Gregor, among many other
    changes, laid out a formal triage process that has been a major influence in
    keeping an organized and healthy support queue.

    We've definitely found that the more support engagement we provide the
    community, the more support comes out of the woodwork.  This is all part of
    supporting a healthy community however, as we have learned.

Stability
    Read the Docs has "grown organically", which is to say it has grown fast,
    unwieldy, and in many directions.  With more proper focus on code quality,
    including clean up efforts, refactoring, and long due upgrades, Read the
    Docs has shed considerable technical debt in the last couple months.  This
    work has already paid off in improving stability and predictability of the
    project.

Ads
    We ran a few tests with advertising on built documentation in the last few
    months.  We discussed at length how we felt about ads and determined our own
    problems with the standard implementation of ads is not the ads themselves,
    but the breach of privacy they signify.

    Because of that, we established that a requirement of us ever showing ads is
    to not use third party tracking.  In fact, we look to remove all third party
    tracking from built documentation as soon as we can.

    To put ads into a clearer context, revenue from in-house ads fully cover our
    costs each month, without asking the community for any further support. It
    probably shouldn't be surprising that advertising revenue is an easier
    income source than seeking donations. We certainly feel Read the Docs
    provides more value than the ads it would serve though. Our last fundraiser
    reflected the value the community puts on the site, and we hope the next
    fundraiser can be as successful.

    Should we ever use ads as a primary revenue source for the community site,
    we have established some rules:

    * We will provide our ads in-house, not through any service that establishes
      third party tracking
    * We will not sell any data about our users
    * We will always prefer ad sponsorship from community members
    * Users that support us through donations or sponsorship are opt out of ads

    Feedback regarding ads has been positive, hopefully our intentions with ads
    has been mostly apparent. We'll be discussing our thoughts on advertising in
    more depth soon, if you have any feedback.

Gold
    We've begun working on a "gold" status feature for users that want to
    support us each month. This will be an optional, recurring subscription to
    Read the Docs. The subscription will provide some additional features for
    users or projects, and some advanced project features might suggest a gold
    subscription for projects that make use of them.

    This idea is still evolving, we'll be asking for more feedback as this
    feature matures.


The next year
-------------

So, let us now set some expectations for the next year forward:

Transparency and feedback
    Operating in the open has been an important tenant to our company since
    formation.  We believe whole-heartedly in the trust and candid feedback it
    provides, and `we have pledged <pledge_>`_ to keep openness and transparency
    at the core of the company.

    Part of the structure that has guided us as a company has been providing
    updates to those that we are accountable to. During our time at PIE, this
    was to our mentors and our peers. Now, we want to be accountable to you, our
    community.

    We would like to continue the periodic updates that started with the
    fundraiser, and we plan on releasing updates, on a quarterly basis, that
    share more insights into the company.  We will continue to expose our goals,
    problems, and decisions to you as we grow and we hope you can provide us
    with your feedback.

.. _pledge: http://www.opencompany.org/about/

Continued work towards stability
    We still have some technical debt that will take a while to pay off,
    but ensuring stability is paramount to having a service we can all rely on.

Support responsiveness
    We will adhere as much as we can to the processes that we established around
    our support channels. We hope that these processes will also allow others in
    the community to easily fill these roles should we need the help.

As for our technical goals, outside our roadmap and continued cleanup and
maintenance, here is what we have on our roadmap:

User experience
    With components becoming more stable, and a generally more stable code base,
    we are shifting focus towards user experience -- the pieces most obvious to
    users. We've made some gains here in the past few months, but have a ways to
    go still.

Easier documentation build tools
    Sphinx is an incredibly powerful tool, but for new users this can be
    overwhelming. We are developing tooling to ease this process for new users
    and provide a solid footing for the majority of use cases. This will also
    help to make the build process more predictable, as this would mimic our
    build backend processes closely.

More reference doc language support
    We have been working towards wider language support for generating API
    reference documentation. Most recently, we worked with Microsoft to develop
    support for `.NET language support in Sphinx <sphinx-dotnet_>`_. This allows
    authors to use existing .NET tooling to generate reStructuredText API
    reference documentation.

.. _sphinx-dotnet: https://github.com/rtfd/sphinxcontrib-dotnetdomain

Let us know
-----------

If you have any feedback or opinions on any of this, continue to let us know.
We're happy to have the feedback.
