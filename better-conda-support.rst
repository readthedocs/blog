.. post:: April 23, 2020
   :tags: conda, builders, science
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      Read the Docs now has more powerful servers and improves the support for
      scientific projects that use conda to build their documentation.


Better support for scientific projects' documentation
=====================================================

In the past year or so, we've been having some issues when building projects' documentation using ``conda``.
These issues were usually the build servers hitting :abbr:`OOM (Out Of Memory)` and failing projects' builds randomly.
Read the Docs has this memory constrain on purpose to avoid misuse of the platform but also to protect other's projects building in the same machine at the same time,
where one project could take over all the memory and make the others to fail.

During this time, we implemented a partial solution around this OOM issue.
We spun up a dedicated server for these kind of projects and we manually assign them to this server on user requests.
This workaround worked during some time, but it involves a bad experience for the user and also us doing a manual setup on demand.
Over the time, we hit again the same issue of OOM even given all the memory available to one project to build its documentation.
After some research, we found that `this is a known issue in the conda community`_ and there are some different attempts to fix it (e.i. `mamba`_).
Unfortunately, none of them became the standard yet and the problem is still there.

.. _this is a known issue in the conda community: https://www.anaconda.com/understanding-and-improving-condas-performance/
.. _mamba: https://quantstack.net/mamba.html

Meanwhile, in another completely different set of work,
we were migrating all of our infrastructure to a different architecture that involves "Azure's Virtual machine scale sets",
usage of the "Azure's Storage accounts" to store all the user's documentation, and remove lot of the state from the servers
(more about this migration coming in a future post).
This helped us to *reduce costs* and allowed us to spun up *bigger instances* for the builders,
made these instances single-process and assign all the memory available to only one project without worrying about affecting others.
Besides that, we also removed the bad user experience of hitting OOM and contacting us to manually assign their project to this servers,
by adding a custom task router that routes small builds to smaller servers, and big builds to these new big servers.
These rules include one to assign ``conda`` projects to be built in the big servers by default.

If you ever had a OOM issue on Read the Docs,
we'd appreciate if you give it a try again and let us know you experience when building scientific documentation.
Besides, if you know that any of your friends were hitting this issue in the past,
we encourage you to talk to them and tell them to give it a try again.

We are willing to have more scientific documentation in our platform and we are putting our grain of sand to make this happen and have better science.
