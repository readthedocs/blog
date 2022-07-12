.. post:: July 12, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - July 2022
====================================

Summer has come,
which means our overall development has slowed a bit as the team takes some well-deserved vacation time.
That said,
we're still excited about our `recent hire`_ and the ongoing work we've been doing to support the documentation ecosystem.

Our focus for Q3 (July-Sept) of 2022 is around improving our frontend and marketing pages. 
This includes a fancy new marketing website, 
as well as a revamped dashboard UX that will make many features nicer for our users.

.. _recent hire: https://github.com/benjaoming


New features
------------

We've continued building a number of features and bug fixes in our roadmap:

- We have shipped an initial set of **Example projects**, which allow users to `get started quickly`_ with Sphinx and MkDocs. We will add more examples in the upcoming month, the first one will be a Jupyter Notebook example. If you have any particular ideas in mind or know of a really cool real-world project that others should check out, please don't hesitate to reach out.
- We added support for **HTML theme authors** to define where our `flyout menu`_ is put in their documentation pages. This is an ongoing effort to allow theme authors to integrate our features nicely into the look & feel of docs.
- **sphinx-hoverxref** works `nicely with Jupyter Book <https://github.com/executablebooks/sphinx-book-theme/issues/577>` now and we `fixed manual references <https://github.com/readthedocs/sphinx-hoverxref/issues/199>`_. 
- We improved the **UX around VCS support and pull request previews**, so that it's more obvious how to enable the notifications on your repository, and warn you if you don't have your account configured correctly.
- To better support security, we have enabled **Content Security Policy headers** on our main dashboard sites. You can contact support if you'd like to enable this on your own documentation domain.
- We have improved our **dashboard translation workflow**, so that translations are now deployed each week, making our site easier to use for many folks around the world.

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

.. _get started quickly: https://docs.readthedocs.io/en/latest/examples.html
.. _flyout menu: https://docs.readthedocs.io/en/latest/flyout-menu.html

Some awesome documentation projects
-------------------------------------------

We are collecting entries for `Awesome Read the Docs Projects`_ - please do tell us about your favorites, either by sending an email or `opening a Pull Request`_!

* `Setuptools`_ has made use of many cool theme settings and displays syntax alternatives in a tabbed interface -- see our `🧵 on Twitter <https://twitter.com/readthedocs/status/1546527820150718469>`_
* `disnake`_ uses many light/dark interface tricks and has added many features for browsing API references -- see our `second 🧵 on Twitter <https://twitter.com/readthedocs/status/1541830875037503489>`_

.. _Setuptools: https://setuptools.pypa.io/en/latest/
.. _disnake: https://docs.disnake.dev/en/latest/
.. _Awesome Read the Docs Projects: https://github.com/readthedocs-examples/.github/
.. _opening a Pull Request: https://github.com/readthedocs-examples/.github/blob/main/contributing.md

Upcoming features
-----------------

- As mentioned above, we are shifting some of our focus to frontend these next few months. Look forward to some links to allow you to test our our new beta dashboard in the next month or two. 
- We are working on a Jupyter/Scientific Python example project, to help users in that ecosystem get their docs started quickly.
- We're continuing to focus on outreach for our new build customization features, so that we can continue to improve them with your feedback.

Possible issues
---------------

- We are actively working to deprecate jQuery from our code, as well as `guide the Sphinx ecosystem <https://github.com/sphinx-doc/sphinx/issues/10608>`_ through the transition. 

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
