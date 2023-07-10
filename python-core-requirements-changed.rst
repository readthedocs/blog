.. post:: July 7, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Python "core requirements" for new projects will install latest version
=======================================================================

Starting on **August 7, 2023** all new projects imported on Read the Docs
will install only ``sphinx``, ``mkdocs`` and ``readthedocs-sphinx-ext`` as "core requirements".
The default behavior will be to install the latest version of these requirements.

Note that previously Read the Docs was installing also
``jinja``, ``sphinx-rtd-theme``, ``pillow``, ``mock``, ``alabaster``, ``commonmark`` and ``recommonmark``
specifying particular versions depending on different factors that were confusing for users and hard to debug.

We are moving away from executing commands and installing dependencies on behalf of the users
and trying to make the build experience on Read the Docs the same as building locally,
without surprises.

Projects imported before August 7, 2023 will keep the existing behavior and won't be affected by this change.
If you have a project you want to install the latest version of these requirements,
you can use a ``requirements.txt`` file to specify their versions, or no version to automatically install the latest version.
Read more about :doc:`how to use a requirements.txt file in our documentation <readthedocs:config-file/v2>`.
