.. post:: April 5, 2021
   :tags: newsletter
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features from April.

Read the Docs newsletter - April 2021
=====================================

This is the first of our monthly newsletters, in which we would like to
openly share with you the most relevant updates of Read the Docs,
offer a summary of what new features we shipped to our users
during the previous month,
and share what things we will be focusing on in the near future.

Company highlights
------------------

-  We have a new colleague! `Juan Luis <https://blog.readthedocs.com/archive/author/juan-luis-cano-rodriguez/>`_
   will be working with us as Developer Advocate, with a focus on fulfilling
   the goals of `the CZI grant we were
   awarded <https://blog.readthedocs.com/czi-grant-announcement/>`_,
   improve our public facing documentation,
   and spread the word about our service.
-  xxx we saw an increment of X % page views
-  We have `a new status page <http://status.readthedocs.com/>`__ so you
   can see the availability history and current status of our infrastructure.

New features
------------

-  There is a `new support form <https://docs.readthedocs.io/en/latest/support.html>`__
   in case you need to send us a request related to your project or
   account, like asking for more resources, change the project slug, and
   so forth.
-  You can now build your project using Python 3.9 by setting your build
   image to ``testing``. Please `open an
   issue <https://github.com/readthedocs/readthedocs.org/issues/new>`__
   if you find any problems with it.
-  Now `all newly created MkDocs projects use the latest version of `mkdocs` by
   default <https://github.com/readthedocs/readthedocs.org/pull/7869>`_. Existing projects can specify a specific version, but won't automatically be upgraded.
-  We expanded a few areas of our user documentation: we added `a brand
   new guide on reproducible
   builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`__,
   considerably improved our `guide on using
   conda <https://docs.readthedocs.io/en/stable/guides/conda.html>`__,
   and `started recommending MyST for writing Markdown with
   Sphinx <https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html#using-markdown-with-sphinx>`__.

You can always see the latest changes to our platforms in our `Read the Docs Changelog <https://docs.readthedocs.io/page/changelog.html>`_ and `Ethical Ad Server Changelog <https://ethical-ad-server.readthedocs.io/page/developer/changelog.html>`_.
Current focus & known issues
----------------------------

-  We have had some availability issues with our commercial hosting for the past few weeks. This was caused by massive I/O load spikes on our web servers, causing increased CPU contention and slower web requests. We tracked the issue down to a background process that was doing a lot of reads from our cloud storage. We have changed our infrastructure so background tasks and web requests are processed by different servers, which has addressed the stability issues. 
-  We were made aware of an open redirect on documentation pages via a report to our `security` address. This was present in our codebase for the last 2 releases, and was fixed in a deployment on Thursday April 1. We'd like to thank Splunk and the Cryptography project for reporting this issue through proper channels. Please always follow our `security reporting guide <https://docs.readthedocs.io/en/latest/security.html>`_ to report potential security issues. 

Upcoming features
-----------------

-  Anthony will work on releasing version 1.0 of ``sphinx_rtd_theme``
   with some changes and deprecations, and outline a plan for future
   releases. He will also be working on our dashboard redesign, which we hope to launch in public beta soon. 
-  On the EthicalAds side, David will focus on more customized ad
   targeting and improvements for the reporting interface.
-  Our new hire, Juan Luis, will work with scientific projects to
   improve their documentation and migrate it to Read the Docs, and
   `start drafting a Sphinx tutorial for
   newcomers <https://github.com/orgs/readthedocs/projects/93>`_.
-  Eric will be split between `hiring a frontend
   developer <https://blog.readthedocs.com/job-frontend/>`_,
   doing project management on `the CZI grant <https://blog.readthedocs.com/czi-grant-announcement/>`_,
   and improving ad performance for our EthicalAds publishers.
-  Manuel, on the other hand, will focus on `Single Sign-On
   Authentication for our commercial
   site <https://docs.readthedocs.io/en/stable/commercial/single-sign-on.html>`_,
   and improving the stability of our deploy process.
-  Installing custom system packages is a very common request, so
   Santos will be working on improving the build configuration, as
   well as formalizing a v3 of our Embed API.
-  And finally, on the commercial side, we’ll work on allowing more
   fine-tuned privacy controls on builds created from pull requests.

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!
