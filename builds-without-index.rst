.. post:: July 20, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Builds with no ``index.html`` at its output's directory are deprecated
======================================================================

Historically, Read the Docs has created an auto-generated ``index.html`` file with minimal instructions about how to setup the project correctly
for those builds that weren't outputting this file.
This auto-generated file has confused more users than helped them.
Mainly, because the behavior on Read the Docs was different from the behavior on their local environment.

Due to this, we decided to stop creating the ``index.html`` file automatically.
Besides, we will check for an ``index.html`` file at the end of the build,
and fail it with a clear message of the problem if there is no ``index.html`` file in the ``$READTHEDOCS_OUTPUT/html`` directory.
This will help users to immediately understand what's the problem and how to solve it.

Builds from projects that are not generating an ``index.html`` file **will start to fail on August 1st at ~9AM PST**, after our regular deploy.
Make sure your project is properly configured and it's creating an ``index.html`` file before that date to avoid unexpected behaviors.

We recommend you following our :doc:`tutorial <readthedocs:tutorial>` to set up your project correctly.

Please, `contact us`_ and let us know any inconvenient you may have with this change.

.. _contact us: mailto:hello@readthedocs.org
