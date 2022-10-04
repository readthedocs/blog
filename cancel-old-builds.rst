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

Read the Docs allows you to keep the documentation always up to date in a simple way
by triggering a new build each time developers push to the repository imported.
This is usually fine, but depending on the developers workflow, there could be situations
where the push are done one immediately after the other making the first builds triggered invalid.

To avoid waiting for those invalid builds to be executed first and finally execute the latest one with the final changes,
we implemented a new feature to cancel those invalid builds and only execute the latest one.
This considerably improves the user experience and also reduce resource costs and energy waste.

More than a month ago,
`we enabled this feature for a subset of projects <https://github.com/readthedocs/readthedocs.org/issues/8961#issuecomment-1231867076>`_
to do a small test before rolling it out to all the projects.
In the past 30 days, we have cancelled around 6k builds on this subset of projects.
The following plot shows cancelled builds per project:

.. image:: /img/cancelled-builds.png
   :align: center
   :width: 100%


Today, we are happy to announce that we decided to enable this feature for all the projects because we have received really good feedback about it
and we noticed a pretty good improvement on the user experience when triggering multiple builds frequently.

Thanks you all for you help while working on this feature and we hope you get a better experience starting today.
Let us know if you find anything not working as expected.
