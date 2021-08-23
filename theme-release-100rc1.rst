.. post:: August 23, 2021
    :tags: theme, release
    :author: Anthony

.. meta::
    :description lang=en:
        Information on the sphinx_rtd_theme pre-release, version 1.0.0rc1, and
        following releases.

Theme release 1.0.0rc1
======================

We are closing in on the next official release of `sphinx_rtd_theme`_, and
we're happy to announce that release candidate version 1.0.0rc1 was
`released to PyPI`_ last week! Project maintainers can contribute to the final
release by `testing the release candidate <Testing_>`_ and raising any potential
bugs on `our issue tracker <issue-tracker_>`_.

The version of our next release was incremented to 1.0.0 due to several
backwards incompatible changes, however this release also adds support for
`Sphinx`_ 4, and fixes several issues stemming from `docutils`_ 0.17.

.. _sphinx_rtd_theme: https://github.com/readthedocs/sphinx_rtd_theme
.. _released to PyPI: https://pypi.org/project/sphinx-rtd-theme/1.0.0rc1/
.. _issue-tracker: https://github.com/readthedocs/sphinx_rtd_theme/issues

.. _Sphinx: https://pypi.org/project/Sphinx/
.. _docutils: https://pypi.org/project/docutils/

Highlights
----------

Here are some of the most significant changes included in release 1.0.0:

Support dropped for old dependencies
    Support is removed for Sphinx versions 1.6 or older, and for Python versions
    3.0 to 3.3. Theme developers no longer test using these versions and
    compatibility is not guaranteed for these versions.

HTML4 support will be dropped soon
    Support for the Sphinx HTML4 writer will be deprecated in release 2.0.

Installation from source won't be supported soon
    Tentatively scheduled for release 3.0, installation from source will no
    longer be a supported installation method. Currently, users are installing
    directly from our GitHub repository, which complicates development of static
    assets.

Support for new dependencies
    The theme now supports Sphinx 4 and docutils 0.17, both the latest in each
    respective release series.

New accessibility features
    Also added were a number of accessibility updates, including better keyboard
    navigation support and more descriptive navigation for screen readers.

Added 4 new translations 
    The theme is close to being almost fully translated in 14 different
    languages. This will provide project maintainers with localized navigation
    elements and accessibility content.

`The theme roadmap <roadmap_>`_ has more information on upcoming releases, and backwards
incompatible changes for each. A full list of changes included in this release
is available in `the theme changelog <changelog_>`_.

.. _roadmap: https://sphinx-rtd-theme.readthedocs.io/en/latest/development.html#roadmap
.. _changelog: https://sphinx-rtd-theme.readthedocs.io/en/latest/changelog.html

Testing
-------

The 1.0.0rc1 release is a pre-release package, meaning it will not install by
default as the most recent release. Project maintainers will need to specify the
release version explicitly to install the release candidate.

In your package's ``extra_requirements``, or a separate ``requirements.txt``
file, you can pin this dependency with:

.. code::

    sphinx_rtd_theme==1.0.0rc1

If you notice any new, unwanted behavior, feel free to open an issue
`on our issue tracker <issue-tracker_>`_.

Upcoming changes
----------------

We have several upcoming releases planned, covered in more depth in
`the theme roadmap <roadmap_>`_.

Of note, our 2.0 release will be dropping support for a number of old
dependencies, including Sphinx versions < 3.0, Sphinx HTML4 writer support,
and Internet Explorer 11.

As the theme moves away from supporting direct installation through our GitHub
repository, we want to preserve development previews of theme releases. In
addition to several more focused releases on the theme roadmap, we will also be
periodically be publishing development releases to PyPI. This will be the
prescribed method to use unreleased theme changes.

Our next official release, currently targeted for October or November, will be
version 1.1. This release will contain additional bug fixes and will be the last
release supporting Sphinx versions less than 3.0. The next planed release will
be version 2.0, in early 2022.

Thanks!
-------

Special thanks to contributor `Blendify`_ for keeping up with support for fresh
dependencies, and new contributor `nienn`_ for helping with bug fixes and the
heavy amount of testing required for this release!

.. _Blendify: https://github.com/Blendify
.. _nienn: https://github.com/nienn
