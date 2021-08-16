:orphan:

Job Posting: Frontend developer with design skills
==================================================

.. |role| replace:: frontend developer

**Update: This role has been filled. If you're interested in working with us, we're always happy to hear from you, but we aren't actively hiring for this role currently.**

.. include:: /hiring/intro.rst

About the job
-------------

This job will be our first |role| hire.
We have a couple members of the team who have some knowledge in this space,
but we hope you will grow to lead our efforts in this area over time.

At the beginning of the year, we received a :doc:`grant to support scientific software</czi-grant-announcement>`.
Given this grant, the job will have two major parts:

* Around half your time will be spent working on work related to scientific software.
  This focuses on improving our documentation embedding client in JavaScript, and working to integrate it into widely used scientific development platforms (eg. Jupyter).
* The other half of your time will be spent working on Read the Docs itself, outside of the grant funding.
  We are working on a site redesign, along with many other places where we have long-standing UX and design issues.

We have two major places that users interact with Read the Docs:

* Our application, where users manage their documentation builds.
* The "documentation pages" which we publish, where 99% of users only read docs, and might not even know Read the Docs is hosting.

Our goal is to improve both of these experiences for our users.

We are working on a full dashboard redesign which is around 80% finished.
One of our first priorities would be for you to come onboard and help us get it finished.
This project will give you a very wide understanding of the platform from the start.

The other major priority with the grant work will be a greenfield implementation of a JavaScript client to embed documentation from the Read the Docs API.
We have some initial prototypes of this work,
but you will be responsible for architecting and shipping this new library for the grant.
We have some ideas on the direction we want to go here,
but you'll have a lot of influence in this major new initiative.

Technical Details
-----------------

Read the Docs is a `large open source web application <https://github.com/readthedocs/readthedocs.org/tree/master/readthedocs>`_.
The current technologies that we're using are:

* Semantic UI for views and styles in our application
* Knockout for view/model binding
* Webpack for bundling of CSS and JavaScript
* Django templates for our application views
* Jinja templates for our marketing content and Sphinx theme design

**You don't need to be familiar with these exact technologies, but having experience with a web-based stack is helpful (eg. Rails, Node, PHP)**.

Our team has more experience with Python and Django than with JavaScript, so our application UI is driven by a hybrid system that primarily relies on application code and Django templates for display. Most of the work that will go into maintaining our application views will be working with Semantic UI inside Django templates, with Knockout  connecting HTML to client side code where client side rendering and interaction is preferred.

Our marketing and landing page content will be a separate project that will use some of the same underlying technologies, but will have very few visual constraints compared to our application. We will be looking for your guidance here in building this project out.

Separate from our application, we also maintain a `widely used Sphinx theme <https://github.com/readthedocs/sphinx_rtd_theme>`_. You'll share some of the maintenance effort on this theme, however it is also a fairly mature project that mostly requires bug fixes.

.. include:: /hiring/details.rst

Applying
--------

We will be accepting applications on an ongoing basis until the position is filled.

**Update: This role has been filled. If you're interested in working with us, we're always happy to hear from you, but we aren't actively hiring for this role currently.**

..
   Please fill out the below form to apply for this role.
   Normal response time is around 2-3 weeks,
   and we intend to reply to all candidates.

   .. raw:: html

       <!-- Make it line up with the content -->
       <div style="margin: .75rem .5rem;">
       <form
         method="POST"
         name="fa-form-1"
         action="https://webhook.frontapp.com/forms/036c4169294f3b04abaa/HAa1z5l3jHnqME6YJDt340VCgxeF8hVDWGjL3gwCaNzOFxR-Rzb62BFANsS4nRAONcsGlfN6TblFZehDKsQAJzck-iEDujTz3-u7vSBo8v8_UN2zeX4xqgQ3ht8"
         enctype="multipart/form-data"
         accept-charset="utf-8"
       >
         <input type="hidden" name="subject" value="Frontend job application">
         <input type="hidden" name="body" value="Content embedded below">

         <div>
           <label for="name">Name</label>
           <input type="text" name="name">
         </div>

         <div>
           <label for="email">Email</label>
           <input type="email" name="email">
         </div>

         <div>
           <label for="timezone">Timezone</label>
           <input type="text" name="timezone">
         </div>

         <div>
           <label for="why">1-2 paragraphs about why you're excited to work on Read the Docs</label>
           <textarea name="why"></textarea>
         </div>

         <div>
           <label for="project">1-2 paragraphs about a project you're proud of</label>
           <textarea name="project"></textarea>
         </div>

         <div>
           <label for="extra">Anything else you'd like us to know?</label>
           <textarea name="extra"></textarea>
         </div>

         <div>
           <label for="resume">Resume/CV</label>
           <input type="file" name="resume">
         </div>

         <div>
           <input type="submit" value="Submit Application">
         </div>
       </form>
       </div>

   Thanks for your interest, and we hope to hear from you soon.
