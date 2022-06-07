.. post:: June 7, 2022
   :tags: newsletter, python
   :author: Eric Holscher
   :location: BND

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - June 2022
====================================

We're excited to welcome `Benjamin Balder Bach`_ to our team,
joining as a part-time contractor for now.
He's a developer with a history of working as an Open Source maintainer and event organizer in the Django community. He has also previously contributed to Read the Docs and will be a wonderful addition to the team.

We're also excited to see people using our new `build.jobs feature`_ that we previously announced.
There are a lot of interesting ways to adapt the build process with this,
and we'll continue to watch with interest how people are using it!

.. _build.jobs feature: https://blog.readthedocs.com/user-defined-build-jobs/
.. _Benjamin Balder Bach: https://github.com/benjaoming


New features
------------

We've continued building a number of features and bug fixes in our roadmap:

- We have shipped a beta implementation of ``build.commands``, which allows users to `fully customize the commands run during builds <https://docs.readthedocs.io/en/latest/build-customization.html#override-the-build-process>`_. This enables support for other documentation tools, and we're excited to see what you can do with it!
- Static files are now served from documentation domains, instead of from ``assets.readthedocs.com``. This allows them to be cached at the CDN with the same rules as all other version-specific files.
- There is a nicer UI for cancelled builds now, which will show as the build status. This will make it more clear when a build failed or was cancelled for some reason.
- We have shipped a new release of `sphinx-hoverxref <https://sphinx-hoverxref.readthedocs.io/en/latest/>`_ with better support for intersphinx content embedding.
- We've shipped support for forced redirects in testing for now. This will allow users to configure redirects that happen when a page exists (200 response), which enables a bunch of neat use cases. `Contact us` if you want to try it out!

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

Upcoming features
-----------------

- We're continuing to focus on outreach for our new build customization features, so that we can continue to improve them with your feedback.
- Our work on improving redirects continues, as we know this is an important feature for many of our users.
- We continue to focus on improving authentication on Read the Docs for Business. We are looking at implementing a two-step login process to simplify a lot of the user experience here.


Possible issues
---------------

- We deprecated a feature flag around Mamba, which is now fully supported via the config file. Projects using Mamba with the old feature flag, and now removed, CONDA_USES_MAMBA, have to update their ``.readthedocs.yaml`` file to use ``build.tools.python: mambaforge-4.10``.
- We are still watching Sphinx upgrades for possible issues they might cause around the ecosystem.

----

Considering using Read the Docs for your next documentation project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
