:orphan:

Job Posting: Frontend developer with design skills
==================================================

.. |role| replace:: frontend developer

.. include:: /hiring/intro.rst

About the job
-------------

This job will be our first |role| hire.
We have a couple members of the team who have some knowledge in this space,
but we will expect you to lead our efforts in this area.

At the beginning of the year, we received a :doc:`grant to support scientific software</czi-grant-announcement>`.
Given this grant, the job will have two major parts:

* For 2021, around half your time will be spent working on work related to our grant.
  This focuses on building a documentation embedding client in JavaScript, and working to integrate it into Sphinx and other widely used platforms.
* The other half of your time will be spent working on Read the Docs itself, outside of the grant funding.
  We are working on a site redesign, along with many other places where we have low-hanging UX and design work.

We have two major places that users interact with Read the Docs:

* Our application, where users manage their documentation builds.
* The "documentation pages" which we publish, where 99% of users only read docs, and might not even know Read the Docs is hosting.

Our goal is to improve both of these experiences for our users.

We are working on a full dashboard redesign which is around 80% finished.
One of our first priorities would be for you to come onboard and help us get it over the line to completion.
You would be working with one of our founders on this project,
and it will give you a very wide understanding of the platform from the start.

The other major priority with the grant work will be a greenfield implementation of a JavaScript client to embed documentation from the Read the Docs API.
We have some initial prototypes of this work,
but you will be responsible for architecting and shipping this new library for the grant.
We have some ideas on the direction we want to go here,
but you'll have a lot of influence in this major new initiative.

Technical Details
-----------------

Read the Docs is a large Python & Django web application.
The current technologies that we're using are:

* Django templates for our application views
* Jinja templates for our marketing content and Sphinx theme design
* Semantic UI for views and styles in our application
* Knockout for view/model binding
* Webpack for bundling of CSS and JavaScript

Our team is has more experience with Python and Django than with JavaScript, so our application UI is driven by a hybrid system that primarily relies on application code and Django templates for display. Most of the work that will go into maintaining our application views will be working with Semantic UI inside Django templates, with Knockout  connecting HTML to client side code where client side rendering and interaction is preferred.

Our marketing and landing page content will be a separate project that will use some of the same underlying technologies, but will have very few visual constraints compared to our application. We will be looking for your guidance here in building this project out.

Separate from our application, we also maintain a widely used Sphinx theme. You'll share some of the maintenance effort on this theme, however it is also a fairly mature project that mostly requires bug fixes.

.. include:: /hiring/details.rst
