.. post:: July 20, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Builds with no ``index.html`` at its output's directory are deprecated
======================================================================

Historically, Read the Docs has created an auto-generated ``index.html`` file with minimal instructions about how to setup the project correctly when your build didn’t output this file.
This auto-generated file has confused more users than it has helped because the behavior on Read the Docs was different from the behavior on their local environment.

To better onboard users, we have deprecated the auto-creation of ``index.html`` files on Read the Docs projects.
We will now check for an ``index.html`` file at the end of the build,
and fail it with a clear message of the problem if there is no ``index.html`` file in the top level of your output directory.

Builds from projects that are not generating an ``index.html`` file **will start to fail on August 1st**.
Make sure your project is properly configured and it’s creating an ``index.html`` file before that date to avoid unexpected behaviors.

We recommend you following our :doc:`tutorial <readthedocs:tutorial/index>` to set up your project correctly.

Please, `contact us`_ and let us know any inconvenient you may have with this change.

.. _contact us: mailto:hello@readthedocs.org
