.. post:: May 5, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - May 2022
===================================

April has been another exciting month here at Read the Docs.
We've gotten a few good candidates for our :doc:`Product-focused Application Developer </job-product-developer/>` job posting,
and we're on to the second round of interviews.
Expect to hear more about any new team members here in the next couple months.

New features
------------

We've continued building a number of features and bug fixes in our roadmap:

- We have launched **CDN with instant cache purging** on the **Pro plan** for our Business users. You can read more about this in our `CDN docs <https://docs.readthedocs.io/en/latest/hosting.html#content-delivery-network-cdn>`_
- Feedback on our latest ``build.jobs`` feature has continued to be great, and we've `improved our documentation <https://docs.readthedocs.io/en/latest/build-customization.html>`_ around this feature.
- We have shipped 404 tracking for our Business users. We're still working to improve this feature by ignoring bot traffic, which is coming soon. You can see it in your :guilabel:`Traffic Analytics` page.
- We have shipped improvements to the security of our build process, which we are not giving specifics on because of the security nature of the work.
- Build notifications (which `you should enable! <https://docs.readthedocs.io/en/latest/build-notifications.html>`_) are not sent when a build is going to be retried, which should keep your inbox a bit cleaner.
- Projects can now use the latest Ubuntu 22.04 LTS release on the configuration file to build their docs: ``build.os: "ubuntu-22.04"``


You can always see the latest changes to our platforms in our :doc:`Read the Docs
Changelog <readthedocs:changelog>`.

.. _check it out: https://docs.readthedocs.io/en/latest/config-file/v2.html#build-jobs
.. _all the options available: https://docs.readthedocs.io/en/latest/builds.html#build-environment

Upcoming features
-----------------

- We are working to improve our user experience around cancelled builds, which we hope will further make things more obvious when a build has failed versus being cancelled for some other reason.
- We're continuing to find new uses for ``build.jobs``, so expect to hear more about this. We're also looking at ways to expand this functionality to other docs tools...
- A lot of users don't know about all the features that we have, so we're going to be introducing a drip email campaign for new users to explain all the various things they can do.
- Redirects are another area where we know our product could be improved, so we'll be tackling that here soon.
- We continue to focus on improving authentication on Read the Docs for Business. We are looking at implementing a two-step login process to simplify a lot of the user experience here.

Possible issues
---------------

- We have some ongoing issues around build retrying that caused issues for a few weeks. We believe these have been fixed.
- There were some small issues with redirects that we have fixed by adding limitations around what can be redirected to. We don't expect this to cause any issues, but wanted to note it.
- We are still watching Sphinx upgrades for possible issues they might cause around the ecosystem.
- We removed the old feature flag ``CONDA_USES_MAMBA``. If your project was using Mamba to create the environment, you should update your configuration file to use ``build.tools.python: mambaforge-4.10`` instead.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _contact us: mailto:hello@readthedocs.org
