.. post:: Nov 1, 2022
    :tags: theme, release
    :author: Ben
    :location: Malmö, Sweden

.. meta::
    :description lang=en:
        Information on sphinx-rtd-theme version 1.1.0


Announcing sphinx_rtd_theme 1.1.0
=================================

We are happy to announce the release of new version of our theme, `sphinx-rtd-theme`_.
In this release, we have focused on bug fixes, backwards compatibility, and making the way for future releases.

.. _sphinx-rtd-theme: https://sphinx-rtd-theme.readthedocs.io/en/stable/


Changes and new features 💄
---------------------------

Visually, we have a couple of small tweaks that most people won't notice unless we mention them here 😇
The objective of the 1.1 release is to maintain backwards compatibility, and that also goes for the visual parts.

* The ``<kbd>`` tag now has a nicer styling.
* Breadcrumb styling has been updated.
* Table cells with multiple paragraphs now have a correct formatting.
* Definition lists are rendered correctly in API docs.
* Issues with citation rendering and styling fixed.
* Long URLs break into several lines instead of overflowing.

.. image:: img/sphinx-rtd-theme-110-screenshot1.png
   :scale: 12%
   :align: right

.. image:: img/sphinx-rtd-theme-110-screenshot2.png
   :scale: 16%
   :align: right

.. image:: img/sphinx-rtd-theme-110-screenshot3.png
   :scale: 16%
   :align: right

In the engine room, we have ensured the long-term stability for users of this theme release by putting upper bounds on ``Sphinx<6`` and ``docutils<0.18``.

We also fixed an issue that caused the theme to fail when Sphinx ``5.2.0.post0`` was released and will ensure that this doesn't happen again.

`Read the full changelog <https://sphinx-rtd-theme.readthedocs.io/en/stable/changelog.html>`_


How to upgrade
--------------

If you are using the theme for the first time, please refer the general `installation instructions <https://sphinx-rtd-theme.readthedocs.io/en/stable/installing.html>`_.

For most projects, including projects hosted on Read the Docs, the general update instruction is to modify your project's dependencies (often stored in ``requirements.txt``) where you should add ``sphinx-rtd-theme==1.1.0`` (or replace any existing entries).

If you have a project on Read the Docs without a Python requirements file ``requirements.txt``, you need to add one in order to use newer versions of sphinx-rtd-theme.
You can read more about adding a ``requirements.txt`` in our :doc:`Documentation about Reproducible Builds <readthedocs:guides/reproducible-builds>`.


.. _sphinx_rtd_theme110_upcoming_releases:

Upcoming releases
-----------------

Each little change comes with an overhead of testing, perfection and a long list of legacy support. We are addressing all that in upcoming releases, so it will become less cumbersome to add new features. The building and testing processes are refined and future releases will drop some of the legacy.

Here are the highlights from our roadmap:

* sphinx-rtd-theme 1.2: `Address jQuery removal from Sphinx <https://github.com/readthedocs/readthedocs.org/pull/9665>`_, `adds docutils 0.18 support <https://github.com/readthedocs/readthedocs.org/pull/9665>`_, possibly also `docutils 0.19 support <https://github.com/readthedocs/sphinx_rtd_theme/pull/1336>`_
* sphinx-rtd-theme 2.0: Adds Sphinx 6.x support, dropping legacy support for several Sphinx releases and old browsers.

If you wish to see more details, `view the full roadmap <https://sphinx-rtd-theme.readthedocs.io/en/stable/development.html#roadmap>`_.


Contributing
------------

If you experience any issues with the theme, we welcome you to visit the GitHub repository `readthedocs/sphinx-rtd-theme <https://github.com/readthedocs/sphinx_rtd_theme/>`_.

For support questions, consider asking in one of the `Read the Docs community support channels <https://dev.readthedocs.io/en/latest/contribute.html#get-in-touch>`_.
