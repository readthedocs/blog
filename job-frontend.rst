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

We have recently gotten a :doc:`grant to support scientific software</czi-grant-announcement>` in 2021.
Given this grant, the job will have two major parts:

* For 2021, around half your time will be spent working on work related to our grant.
  This focuses on building a generic content embedding client in Javascript, and working to integrate it into Sphinx and other widely used platforms.
* The other half of your time will be spent working on Read the Docs itself, outside of the grant funding.
  We are working on a site redesign, along with many other places where we have low-hanging UX and design work.

We have two major places that users interact with Read the Docs:

* The "dashboard" where users manage their documentation builds.
* The "documentation pages" which we publish, where 99% of users only read docs, and might not even know Read the Docs is hosting.

Our goal is to improve both of these experiences for our users.

We are working on a full dashboard redesign which is around 80% finished.
One of our first priorities would be for you to come onboard and help us get it over the line to completion.
You would be working with one of our founders on this project,
and it will give you a very wide understanding of the platform from the start.

The other major priority with the grant work will be a green-field implementation of a Javascript client to embed documentation.
We have some initial prototypes of this work,
but you will be responsible for architecting and shipping this new library for the grant.
We have some ideas on the direction we want to go here,
but you'll have a lot of influence of this major new initiative.

Technical Details
-----------------

Read the Docs is a large Python & Django web application.
The current technologies that we're using are:

* Django/Jinja templates
* Webpack for bundling
* Semantic UI for components

TODO: Write a bit more about our "frontend philosophy"

.. include:: /hiring/details.rst
