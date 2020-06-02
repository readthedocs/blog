.. post:: April 28, 2020
   :tags: conda, builders, science
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      Read the Docs now has more powerful servers and improves the support for
      scientific projects that use conda to build their documentation.


Better support for scientific project documentation
===================================================

In the past year, we've been having issues when building projects' documentation using ``conda``.
Our build servers were running out of memory and failing projects' builds.
Read the Docs has this memory constraint to avoid misuse of the platform,
causing a poor experience for other users.

Our first solution was a dedicated server for these kind of projects.
We would manually assign them to this server on user requests.
This workaround worked okay, but it involves a bad experience for the user and also us doing a manual step each time.
Over time, we hit again the same issue of OOM, even giving all the memory available to one project to build its documentation.
After some research, we found that `this is a known issue in the conda community`_ and there are some different attempts to fix it (like `mamba`_).
Unfortunately, none of them became the standard yet and the problem is still there.

.. _this is a known issue in the conda community: https://www.anaconda.com/understanding-and-improving-condas-performance/
.. _mamba: https://quantstack.net/mamba.html

Meanwhile, in another completely different set of work,
we were migrating all of our infrastructure to a different architecture:

* Azure *Virtual machine scale sets* for autoscaling our servers,
* Azure *storage accounts* to store all the user's documentation
* Proxito, an internal service to remove a lot of the state from our servers (more about this migration coming in a future post)

This helped us to *reduce costs* and allowed us to spin up *bigger instances* for the builders.
We have also made some other important operational changes:

* Our builders are now single-process, giving all the memory available to only one project without worrying about affecting others.
* We added `custom task router`_ that routes small builds to small servers (3GB RAM), and big builds to larger servers (7GB RAM). This removes the need for users to ask us to upgrade their isntances.
* Assigned all ``conda`` projects to be built by big servers by default.

If you ever had a memory issue on Read the Docs,
we'd appreciate if you give it a try again.
Please `let us know`_ about your experience when building scientific documentation.
If you know that any of your friends were hitting this issue in the past,
we encourage you to talk to them and tell them to give it a try.

We are excited to have more scientific documentation on our platform and we are doing our small part to make this happen and have better science in the world.

.. _custom task router: https://github.com/readthedocs/readthedocs.org/blob/8e78d680d02aeba12644796b979ef62459f64932/readthedocs/builds/tasks.py#L11
.. _let us know: mailto:support@readthedocs.org
