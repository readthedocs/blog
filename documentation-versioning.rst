.. post:: July 23, 2019
   :tags: vcs, versioning
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:

      Recommendations about how to do documentation versioning.

Documentation Versioning: Good Practices
========================================

Project releases and documentation versions are strongly related each other.
We usually want to have a release ``1.0.3`` with it's own documentation version ``1.0.3`` that's specific for that release.

In practice, when we make a new release of our software,
we create a new tag in our :abbr:`VCS` for this release and activate this new version on Read the Docs.
At this point, Read the Docs will build and publish the new documentation version ``1.0.3`` for us.

This approach of "VCS tag" mapped to a "Read the Docs version" works in most of cases.
Although, there could be some problems that may arise in time and that we can prevent using a different strategy.


Problems of using tags for documentation versions
-------------------------------------------------

The main problem of using VCS tags to build documentation versions is that they are static.
This means, that once the tag is created it will never be modified.

This may not seems like a problem at first sight since that's the main concept of :abbr:`VCS` tags.
Although, when talking about documentation versions,
sometimes happen that after making a release there is a typo in the docs, or a small code example that does not work,
or a sentence that is confusing, etc. and we want to fix it to avoid this inconveniences.

Making a new tag and release just for these small changes does not worth the effort but also it may confuse our users.
In other words, having a ``1.0.4`` release that only fixes a sentence in the documentation is not optimal.

Another problem that we have found with this approach is when new features are released on Read the Docs.
Applying this feature to all of our documentation versions --new ones and old ones, it's a problem.
Similarly, if we want to install a new Sphinx extension in all our versions,
update one of its settings, change the theme,
or even change a build config in the `.readthedocs.yml`_,
we will be "blocked" by the tags being static.


Recommended versioning strategy
-------------------------------

The workflow that we recommend to versioning your documentation is by having release branches instead.
With this approach, if a reader detects a typo in the documentation,
we can just fix the typo and commit and push to this ``1.0.x`` release branch.
By doing this, the documentation will be automatically updated and published on Read the Docs.

Following our example, this strategy would be:

* ``1.0.x`` is a release branch for the ``1.0`` version
* ``1.0.3`` is a similar tag for your ``1.0.x`` branch, with the latest release
* ``1.0.0`` is the first tag for your ``1.0.x`` branch.


In summary
----------

It's a good idea to have a plan about versioning our software and documentation before going to far.
Knowing the limitation on the different strategies will give us more context to make a better decision.
This will avoid us headaches in the future or even re-tagging :abbr:`VCS` tags just to fix small documentation issues.

Happy versioning!

.. _.readthedocs.yml: https://docs.readthedocs.io/page/config-file/v2.html
