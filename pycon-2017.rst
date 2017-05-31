.. post:: May 31, 2017
   :tags: pycon, sprints
   :author: Anthony

PyCon 2017 in Review
====================

Things are finally getting back to normal for us after another very busy PyCon.
It's always wonderful seeing old friends and getting a chance to meet new
friends from the community. PyCon provides a great outlet to talk to others in
our community about the problems we all face as open source developers and open
source companies -- like funding, sustainability, and building community. We are
sad to see PyCon leave Portland, but luckily PyCascades_ will soon be filling
the void left in Cascadia_ after PyCon moves on.

.. _Cascadia: https://en.wikipedia.org/wiki/Cascadia_(bioregion)
.. _PyCascades: http://www.pycascades.com/

This year, we announced official sprints on Read the Docs during the sprint
week following PyCon. We focused our sprint efforts on code cleanup, in order
to avoid the problems on-boarding new contributors we normally face as a large
project.

The sprints went surprisingly well this year. We were able to enlist the help
of several new contributors during sprints, and folks didn't waste any time
diving into the code. It was a large relief to finally spend some time
addressing code cleanup and removal. **Contributors were able to create and
merge 38 pull requests over the week**, and we're still wrapping up work on
several other pull requests. Our work focused on several areas in particular:

Linting strictness
    When we started a serious effort to lint our codebase, we decided to address
    linting incrementally. We currently do a primary pass with low strictness,
    and a second pass of higher strictness only on select paths. During the
    sprints, contributors were able to pick off and focus on a single Django
    application. Cumulatively, contributors were able to fix linting issues
    across all of our applications and we're very close to again raising our
    strictness application-wide.

Code removal
    Several contributors moved on to hunting down and removing some unused code
    and dependencies. Having started with linting and testing problems, these
    contributors seemed well primed to understanding more complex parts of our
    code. We were able to remove several unused legacy pieces of code and some
    unused dependencies as a result.

Python 3
    Contributor gthank_ started porting Read the Docs to Python 3 before the
    sprints, and was able to drop by our sprint to debug some problems with
    porting. We've been wanting to port to Python 3 for years now, but
    unfortunately, we could never justify this work as the core team. This pull
    request is still a work in progress, but we anxiously await being able to
    make the switch to Python 3.

As the Read the Docs core team is small, we can't easily justify using our time
to focus on long standing issues with code quality, so the PyCon sprints were a perfect
opportunity to focus on this type of clean up. Our codebase is complex and
unwieldy to new contributors, so focusing on linting and testing allowed
contributors to jump in without having to spend the better part of a day setting
up our full stack.

We were very gracious to have all of this help. A big thanks once again to all
of our new contributors who stuck around and contributed:

* cmc333333_
* lordmauve_
* fmoor_
* smcoll_
* gthank_

PyCon has now wrapped up, but our next stop this summer is `DjangoCon 2017`_ in
Spokane, WA. We look forward to seeing some more of you there and hopefully
working with some of you to sprint on Read the Docs again!

.. _cmc333333: https://github.com/cmc333333
.. _lordmauve:  https://github.com/lordmauve
.. _fmoor: https://github.com/fmoor
.. _smcoll: https://github.com/smcoll
.. _gthank: https://github.com/gthank

.. _DjangoCon 2017: https://2017.djangocon.us/
