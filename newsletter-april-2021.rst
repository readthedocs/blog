.. post:: April 6, 2021
   :tags: newsletter, python
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

-  We have a new colleague! `Juan Luis`_
   will be working with us as Developer Advocate, with a focus on fulfilling
   the goals of `the CZI grant we were
   awarded <https://blog.readthedocs.com/czi-grant-announcement/>`_,
   improve our public facing documentation,
   and spread the word about our service.
-  The average daily pageviews went up by 9.4 % from the previous month.
-  We have `a new status page <https://status.readthedocs.com/>`_ so you
   can see the availability history and current status of our infrastructure.

.. Pageviews stats obtained from Google Analytics, https://readthedocs.io property,
   and divided by the total number of days in the month

New features
------------

-  There is a `new support form <https://docs.readthedocs.io/en/latest/support.html>`_
   in case you need to send us a request related to your project or
   account, like asking for more resources, change the project slug, and
   so forth.
-  You can now build your project using Python 3.9 by setting your build
   image to ``testing``. Please `open an
   issue <https://github.com/readthedocs/readthedocs.org/issues/new>`_
   if you find any problems with it.
-  Now `all newly created MkDocs projects use the latest version of mkdocs by
   default <https://github.com/readthedocs/readthedocs.org/pull/7869>`_.
   Existing projects can specify a specific version, but won't automatically
   be upgraded.
-  We expanded a few areas of our user documentation: we added `a brand
   new guide on reproducible
   builds <https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html>`_,
   considerably improved our `guide on using
   conda <https://docs.readthedocs.io/en/stable/guides/conda.html>`_,
   and `started recommending MyST for writing Markdown with
   Sphinx <https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html#using-markdown-with-sphinx>`_.
-  We also cleaned up some old contribution documentation, and renamed
   `our installation instructions <https://docs.readthedocs.io/en/stable/development/install.html>`_
   for clarity. Now Docker Compose is our recommended method to install
   Read the Docs, which will make contributing easier.
-  We added the possibility to declare `publicly visible environment
   variables <https://github.com/readthedocs/readthedocs.org/pull/7891>`_.

You can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_ and `Ethical Ad Server
Changelog <https://ethical-ad-server.readthedocs.io/page/developer/changelog.html>`_.

Current focus & known issues
----------------------------

-  We have had some availability issues with our commercial hosting for the past
   few weeks. This was caused by massive I/O load spikes on our web servers,
   causing increased CPU contention and slower web requests. We tracked the issue
   down to a background process that was doing a lot of reads from our cloud
   storage. We have changed our infrastructure so background tasks and web
   requests are processed by different servers, which has addressed the stability
   issues.
-  We were made aware of an `open redirect on documentation
   pages <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-625x-cj64-6j7h>`_
   via a report to our ``security`` address. This was present in our codebase for the
   last 2 releases, and was fixed in a deployment on Thursday April 1. We'd like
   to thank Splunk and the Cryptography project for reporting this issue through
   proper channels. Please always follow our `security reporting guide
   <https://docs.readthedocs.io/en/latest/security.html>`_ to report potential
   security issues.

Upcoming features
-----------------

-  `Anthony`_ will work on releasing version 1.0 of ``sphinx_rtd_theme``
   with some changes and deprecations, and outline a plan for future
   releases. He will also be working on our dashboard redesign, which we hope
   to launch in public beta soon.
-  On the EthicalAds side, `David`_ will focus on improving our contextual ad targeting
   and improvements for the reporting interface.
-  `Eric`_ will be split between `hiring a frontend
   developer <https://blog.readthedocs.com/job-frontend/>`_,
   doing project management on `the CZI
   grant <https://blog.readthedocs.com/czi-grant-announcement/>`_,
   and improving ad performance for our EthicalAds publishers.
-  Our new hire, `Juan Luis`_, will work with scientific projects to
   improve their documentation and migrate it to Read the Docs, and
   `start drafting a Sphinx tutorial for
   newcomers <https://github.com/orgs/readthedocs/projects/93>`_.
-  `Manuel`_, on the other hand, will focus on `Single Sign-On
   Authentication for our commercial
   site <https://docs.readthedocs.io/en/stable/commercial/single-sign-on.html>`_,
   and improving the stability of our deploy process.
-  Installing custom system packages is a very common request, so
   `Santos`_ will be working on improving the build configuration, as
   well as formalizing a v3 of our Embed API.
-  And finally, on the commercial side, we’ll work on allowing more
   fine-tuned privacy controls on builds created from pull requests.

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Anthony: https://github.com/agjohnson
.. _David: https://github.com/davidfischer
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
