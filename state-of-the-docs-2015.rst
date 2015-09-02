.. post:: Sep 1, 2015
   :tags: report
   :author: Anthony

State of the Docs
=================

August has historical significance for Read the Docs, so it seemed fitting to
wrap up August by taking a moment to step back and reflect on what we've done in
the last year.

What makes August so significant to us?

For starters, this August saw the *5th birthday of Read the Docs*!
We're still humbled by the project's success,
and the important role it continues to play for old and new users alike.

This growth has been difficult to manage at a few points,
especially when there hasn't focused support given back to the community.
Though the project always had core maintainers,
for Read the Docs to continue growing as a community resource,
we knew it required dedicated attention.

This is the reason why, in August of last year,
Eric and I set out to create a company around Read the Docs -- another
significant bookmark in Read the Docs' history.

At this time last year, we had just `formed Read the Docs, Inc`_,
we were fresh into the `PIE accelerator program`_,
and we were planning how to bring our documentation values to companies that
weren't open source.

Our goal when starting the company, which stands today,
was to raise the value of documentation,
both inside companies and in open source communities.

The last year
-------------

Here are some of the major decisions that we made as a company in the last year.

Treat the community site as a separate entity
    This goes back to the formation of Read the Docs, Inc.,
    where we protected the community site from interests in the for profit
    side -- that is, in readthedocs.com.

    Part of defining these two as entities requires us as core maintainers to
    explicitly put on different hats -- though this is still something we are
    struggling with and will continue to struggle with.
    We haven't gone as far as to strictly track the time we take off one of our
    many business development hats and put on our community support or
    maintainer hat.
    However, doing so would allow us to define the true costs
    of the community site, and where our income should come from.

    Instead, we currently spend enormous amounts of time supporting the
    community site, a full-time job in its own right, and treat ourselves as
    contractors to the community site.

    In the future, and in our grand vision, the community site would eventually be
    able to structure as a 501c non-profit entity, separate from the for-profit
    interests. This would allow for more incentive for larger donations to our
    support costs. This however, doesn't make financial sense quite yet.

Our support fundraiser
    In order to make the community site more sustainable,
    we decided to call on our community for support back in June.
    Our goal was to make improvements on the site that we were having trouble making by just ourselves,
    and to fund everyone's time in doing so.

    Thanks to all the contributors from our community, we raised our goal
    of $24,000,
    and were able to fund the time of multiple engineers working steadily on
    Read the Docs for the last few months.

    We already outlined our costs and our plans behind our June fundraiser in a previous
    post. We will be following up the last few months of work with an
    overall review of the fundraiser and the work we performed in the coming
    weeks.

Triaging
    Hopefully, our support responsiveness has been more apparent.
    One hurdle in bringing on more engineers, and engaging the community more,
    was the lack of formal ticketing and open decision making.
    Gregor, among many other changes, laid out a formal triage process
    that has been a major influence in keeping an organized and healthy support
    queue.

    We've definitely found that the more support engagement we provide the community,
    the more support comes out of the woodwork.
    This is all part of supporting a healthy community however,
    as we have learned.

Stability
    Read the Docs has "grown organically",
    which is to say it has grown fast, unwieldy, and in many directions.
    With more proper focus on code quality, including clean up efforts,
    refactoring, and long due upgrades, Read the Docs has shed considerable
    technical debt in the last couple months.
    This work has already paid off in improving stability and predictability of
    the project.

Gold
    We decided to adopt a "gold" status feature model for users that want to
    support us each month.
    This is an optional, recurring subscription to Read the Docs.

    We have plans to make gold subscriptions more functional,
    but for now, it is just a way to show your support of Read the Docs.

Ads
    We ran a few tests with advertising on built documentation in the last few
    months.
    We discussed at length how we felt about ads and determined our own problems with the
    standard implementation of ads is not the ads themselves,
    but the breach of privacy they signify.

    Because of that, we established that a requirement of us ever showing ads is
    to not use third party tracking.  In fact, we look to remove all
    third party tracking from built documentation as soon as we can.

    To put ads into a clearer context,
    revenue from in-house ads fully cover our costs each month,
    without asking the community for support.
    It probably shouldn't be surprising that advertising revenue is an easier income source
    than seeking donations.
    We certainly feel Read the Docs provides more value than the ads it would
    serve though.
    Our last fundraiser reflected the value the community puts on the site,
    and we hope the next fundraiser can be as successful.

    Should we ever use ads as a primary revenue source for the community
    site, we have established some rules:

    * We will provide our ads in-house, not through any service that establishes
      third party tracking
    * We will not sell data about our users
    * We will always prefer ad sponsorship from community members
    * Users that support us through gold or sponsorship are opt out of ads

    Feedback regarding ads has been positive,
    hopefully our intentions with ads has been mostly apparent.

The next year
-------------

So, let us now set some expectations for the next year forward:

Monthly updates
    Part of the structure that has guided us as a company has been providing
    updates to those that we are accountable to. During our time at PIE, this
    was to our mentors and our peers. Now, we want to be accountable to you, our
    community.

    Expect the monthly updates that started with our fundraiser to continue,
    albeit, more on time.

Continued work towards stability
    We still have some technical debt that will take a while to pay off,
    but ensuring stability is paramount to having a service we can all rely on.

More insight into our operations
    `Operating in the open`_ has been an important tenant to our company since
    formation.  We believe whole-heartedly in the trust and candid feedback it
    provides.  We will continue to expose our thoughts, problems, and decisions
    to you as we continue to grow.

Support responsiveness
    We will adhere as much as we can to the processes that we established around
    our support channels. We hope that these processes will also allow others in
    the community to easily fill these roles.

As for our technical goals outside our roadmap and continued cleanup and
maintenance:

User experience
    With components becoming more stable, and a generally more stable
    code base, we are shifting focus towards user experience -- the pieces most
    obvious to users. We've made some gains here in the past few months, but
    have a ways to go still.

Easier documentation build tools
    Sphinx is an incredibly powerful tool, but for new users this can
    be overwhelming. We are developing tooling to ease this process for new
    users and provide a solid footing for the majority of use cases.

More reference doc language support
    We have been working towards wider language support for generating API
    reference documentation. Most recently, we worked with Microsoft to develop
    support for .NET language support in Sphinx. This allows authors to use
    existing .NET tooling to generate reStructuredText API reference
    documentation.

Supporting Read the Docs
------------------------

If you are wondering how you can continue to support us, here are a few ways.

If you are an open source contributor,
or someone else who benefits regularly from Read the Docs,
contributions or a gold subscriptions will go a long ways.

We know the troubles with financing open source software however.
Whether you can contribute or not,
continue bringing your projects to Read the Docs.
We value spreading great, open documentation above all.

You can also consider contributing to any of our projects.
Consider helping with support, code cleanup on Read the Docs,
or extending community support for reference documentation generation.
We are always willing to point you in a direction to get started contributing.

If you are a company, or work for a company, that uses Read the Docs to host
documentation, consider a subscription or better yet, a plan hosting with readthedocs.com.
Though some companies are comfortable with our free, open source hosting,
companies will be better served, and have access to business-class support, on readthedocs.com.

We're always welcome to feedback and input on anything we're doing.
If you have some thoughts on any of this, we'd love to hear it.
