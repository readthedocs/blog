.. post:: July 23, 2019
   :tags: versioncontrol, documentation
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:

      Recommendations about how to do documentation versioning.

Documentation Versioning: Best Practices
========================================

Project releases and documentation versions are strongly related each other.
You usually want to have a release ``1.0.3`` with it's own documentation version ``1.0.3`` for that specific release.

When you make a new release of your software,
you create a new tag in your :abbr:`VCS (Version Control System)` for this release and activate this new version on Read the Docs.
At this point, Read the Docs will build and publish the new documentation version ``1.0.3`` for you.

This approach of "VCS tag mapped to a Read the Docs version" works in most cases.
There are sometimes problems with this approach that we can prevent using a different strategy.


Problems of using tags for documentation versions
-------------------------------------------------

The main problem of using VCS tags to build documentation versions is that they are *static*.
Once a tag is created it can never be modified. [#]_

This may not seem like a problem at first, since that's the main concept of VCS tags.
When talking about documentation versions,
sometimes after making a release there is a typo in the docs, or a small code example that doesn't work,
and you want to fix it.

Making a new tag just for these small changes isn't worth the effort, and also it can confuse users.

Another problem that we have found with this approach is when new features are released on Read the Docs.
Adding this new feature to all of your documentation versions is impossible.
Similarly, if you want to install a new Sphinx extension in all your versions,
update one of its settings, change the theme,
or even change a build config in the `.readthedocs.yml`_,
you will be "blocked" by the tags being static.


Recommended versioning strategy
-------------------------------

**The workflow we recommend for versioning your documentation is having release branches.**
With this approach, if a reader detects a typo in the documentation,
you can just fix the typo and commit and push to this ``1.0.x`` release branch.
By doing this, the documentation will be automatically updated and published on Read the Docs.

Following our example, this strategy would be:

* ``1.0.x`` is a release branch for the ``1.0`` version
* ``1.0.3`` is a similar tag for your ``1.0.x`` branch, with the latest release
* ``1.0.0`` is the first tag for your ``1.0.x`` branch.


In summary
----------

It's a good idea to have a plan about versioning your software and documentation before going too far.
Knowing the limitations on the different strategies will give you more context to make a better decision.
This will avoid you headaches in the future or even re-tagging VCS tags just to fix small documentation issues.

Happy versioning!

.. _.readthedocs.yml: https://docs.readthedocs.io/page/config-file/v2.html
.. [#] It's technically possible, but not recommended by all packaging tools
