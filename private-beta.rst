.. post::
   :tags: beta
   :category: drafts
   :author: Anthony

Private Beta Read the Docs for Business
=======================================

.. Float the signup to the right.
.. raw:: html

    <div style="float: right; margin: 1em; margin-top: 0em;">

.. image:: img/logo.png
    :width: 200

.. raw:: html

      <form method="GET"
            action="https://readthedocs.com/accounts/signup">
        <input type="submit"
               value="Request a Beta Invite" />
      </form>
    </div>

Just last Friday,
this year's class at `PIE`_ culminated with `PIE's Demo Day`_.
We've been in `PIE`_ for three months so far,
building features on top of `Read the Docs`_ for companies,
an offering that will help provide development and support for all users of Read the Docs.
On Friday, we announced that we are now offering a private beta,
for `Read the Docs for Business`_.

Our primary requirement when we started this journey was to only affect
`Read the Docs`_ *for the better*.
Our ideals didn't align with the traditional startup,
which seemed contradictory to supporting open source communities.
We envisioned a business that was a life-style business more than a startup,
and what we call success is funding full time development and support on Read the Docs,
*not* being acquired.

We've spent our time in PIE building up our business,
and along with tremendous help from PIE and all of our mentors,
planning it's future path.
Our development focus has mostly been on building the following features,
for open source users, but also for companies.

.. _Read the Docs for Business: https://readthedocs.com
.. _readthedocs.org: https://readthedocs.org
.. _Read the Docs: https://readthedocs.org
.. _PIE: http://piepdx.com
.. _PIE's Demo Day: http://blog.piepdx.com/2014/10/17/pies-2014-demo-day/

Organizations and Teams
-----------------------

`Read the Docs`_ has the notion of co-maintainers,
a standard used by open source communities.
But this doesn't work as well for companies,
where central access control is required and projects are often owned by teams.
Aside from user access control,
organizations, teams, and sharing support will control who has access to your documentation.
Companies can give access to teams, members, or people outside their organization completely.

Private Documentation
---------------------

We spent a lot of time figuring out how to handle private documentation correctly.
It's a large departure from what we're doing on `readthedocs.org`_,
where the vast majority of our users don't even have an account.
Though companies might publicly host documentation to support software they maintain or sell,
more universally, companies need to host documentation privately.
This required secure access, transfer, and handling of private repositories,
as well as security features to make the documentation build process secure.

Search
------

Our hope is to make finding documentation as easy as possible,
because poor search capabilities is one of our largest gripes with how documentation is used today.
We've started by making documentation that can be searched by facet,
with basic support for searching documentation type.

Markdown Support
----------------

We love `rST`_, especially when paired with `Sphinx`_,
but `Markdown`_ support is a common request we've wanted to address for some time now.
Communities are already using Markdown for their documentation efforts,
so we wanted to add indexing and search to make Markdown documentation highly usable.
One-step setup from Github is supported with Markdown,
so now, you can easily get started on `Read the Docs`_ with your existing documentation.

.. _rST: http://docutils.sourceforge.net/rst.html
.. _Sphinx: http://sphinx-doc.org/
.. _Markdown: http://daringfireball.net/projects/markdown/syntax

Beta Invite
-----------

Our private beta is now open,
we'd like to welcome you to join us in writing great documentation.
We're slowly rolling out access to the private beta,
you can sign up below and we'll contact you soon with access.

.. raw:: html

    <form method="GET"
          action="https://readthedocs.com/accounts/signup">
      <input type="submit"
             value="Request a Beta Invite" />
    </form>

Also, here's the video of Eric's pitch from `PIE's Demo Day`_,
be sure to check it out,
along with `some of the other groups`_ in this year's class.

.. _some of the other groups: https://www.youtube.com/playlist?list=PLFDgm_9P62ut5sSOPTMMoiz8Xb2z-nJdz

.. raw:: html

    <iframe width="560"
            height="315"
            src="http://www.youtube.com/embed/U6ueKExLzSY?list=PLFDgm_9P62ut5sSOPTMMoiz8Xb2z-nJdz"
            frameborder="0"
            allowfullscreen></iframe>
