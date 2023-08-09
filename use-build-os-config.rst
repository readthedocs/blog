.. post:: August 9, 2023
   :tags: builders, deprecation
   :author: Manuel
   :location: BCN
   :category: Changelog


Use ``build.os`` instead of ``build.image`` on your configuration file
======================================================================

We are announcing the deprecation of ``build.image`` config key in favor of ``build.os``.
Read the Docs *will start requiring* a ``build.os`` config key for all projects in order to build documentation successfully.
**We will start failing builds using "build.image" on their config file on October 16, 2023**.


Deprecation timeline
--------------------

We understand this change will affect many of our users,
so we have a timeline to communicate this deprecation to our users effectively.

* **Monday, August 28, 2023**: Do the first brownout (temporarily enforce this deprecation) for 12 hours: 00:01 PST to 11:59 PST (noon)
* **Monday, September 18, 2023**: Do a second brownout (temporarily enforce this deprecation) for 24 hours: 00:01 PST to 23:59 PST (midnight)
* **Monday, October 2, 2023**: Do a third and final brownout (temporarily enforce this deprecation) for 48 hours: 00:01 PST to October 3, 2023 23:59 PST (midnight)
* **Monday, October 16, 2023**: Fully remove support for building documentation using "build.image" on the configuration file


Migrating to ``build.os``
-------------------------

If you have a project on Read the Docs that is using ``build.image``,
**you will need to migrate to the new config key as soon as possible** to continue building your project.

There are some small differences between ``build.image`` and ``build.os`` that we detail here:

- ``version: 2`` must be used with ``build.os``
- To specify the Python version, you have to use ``build.tools.python``

Below is an example of a valid ``build`` section of your configuration.
Make sure to make these changes before **October 16, 2023**:


.. code:: yaml

   version: 2
   build:
     os: "ubuntu-22.04"
     tools:
       python: "3.11"

You can read about the ``build.os`` key, including all possible values, in our `"build.os" documentation <https://docs.readthedocs.io/en/stable/config-file/v2.html#build-os>`_.

Contact us
----------

`Contact us`_ if you have any questions,
and let us know if you are having trouble using a this new config key for any reason.

.. _Contact us: https://readthedocs.org/support/
