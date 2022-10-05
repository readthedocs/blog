.. post:: October 4, 2022
   :tags: builds, ci
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      A new feature that auto-cancels invalid builds was deployed. It improves the user experience,
      reduces resource costs and also energy waste.

Auto-cancel invalid builds
==========================

Read the Docs allows you to keep your documentation up to date in a simple way,
by triggering a new build each time developers push a git repository. 
Depending on the your workflow, there could be situations
where multiple pushes are done during a short time window.
This causes a situation where you have to wait a long time for a build that will be immediately overwritten.

To avoid waiting for those builds to be executed,
we implemented a new feature to cancel these useless builds and only execute the latest one.
This considerably improves the user experience and also reduces resource costs and energy waste.

More than a month ago,
`we enabled this feature for a subset of projects <https://github.com/readthedocs/readthedocs.org/issues/8961#issuecomment-1231867076>`_
to do a small test before rolling it out to all the projects.
In the past 30 days, we have cancelled around 6k builds on this subset of projects.
The following plot shows cancelled builds per project:

.. image:: /img/cancelled-builds.png
   :align: center
   :width: 100%


Today, we are happy to announce that we are enabling this feature for all the projects.
We have received really good feedback from our test users,
particularly around the user experience when triggering multiple builds frequently.

We appreciate the feedback that our test users gave us,
and we're excited to roll this out to all our users.
Please let us know if you any new issues around cancelled builds as we roll out this feature more widely.
