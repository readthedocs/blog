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

- We have shipped an initial set of **Example projects**, which allow users to `get started quickly`_ with Sphinx and Mkdocs. We're excited to continue to build more example projects to help folks bootstrap their docs projects.
- We added support for **HTML theme authors** to define where our `flyout menu`_ is put in their documentation pages. This is an ongoing effort to allow theme authors to integrate our features nicely into the look & feel of docs.
- We improved the **UX around VCS support and pull request previews**, so that it's more obvious how to enable the notifications on your repository, and warn you if you don't have your account configured correctly.
- To better support security, we have enabled **Content Security Policy headers** on our main dashboard sites.
- We have improved our **dashboard translation workflow**, so that translations are now deployed each week, making our site easier to use for many folks around the work. 

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

.. _get started quickly: https://docs.readthedocs.io/en/latest/examples.html
.. _flyout menu: https://docs.readthedocs.io/en/latest/flyout-menu.html


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

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
