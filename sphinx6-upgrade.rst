.. post:: January 4th, 2023
   :tags: sphinx, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Sphinx 6 is out. We share our considerations about upgrading.


Sphinx 6 is out and has important breaking changes
==================================================

Sphinx 6 was released on December 29, 2022.
It contains a few major breaking changes that users should be aware of,
and some smaller new features as well.
Here are some of our considerations for the upgrade process:

- Python 3.8+ is required. To enable this on Read the Docs, you will need to specify a Python version using the :ref:`readthedocs:config-file/v2:build.tools.python` setting. If it's possible for your project, you can make the jump all the way to Python 3.11.
- Support is dropped for docutils 0.14, 0.15, 0.16 and 0.17. It now supports only docutils 0.18 or 0.19.
- `sphinx-rtd-theme`_ will support Sphinx 6 from 1.2.0, including docutils 0.18.
  You can already install the release candidate: ``pip install sphinx-rtd-theme==1.2.0rc2``.
- Bundled jQuery is removed.
  The JavaScript asset is easily added back using the new extension `sphinxcontrib-jquery`_.
  It is included automatically by `sphinx-rtd-theme`_, so if you are using our theme,
  you will also continue to have jQuery available in your documentation.
- All bundled JavaScript was removed, including also underscore.js.

For more information and full details you can read the `Sphinx changelog <https://www.sphinx-doc.org/en/master/changes.html#release-6-0-0-released-dec-29-2022>`_

Since most documentation projects rely on themes and extensions,
we recommend checking for Sphinx 6 support in those projects before upgrading.

.. _sphinxcontrib-jquery: https://pypi.org/project/sphinxcontrib.jquery/


Possible issues
---------------

* Sphinx 6.0 and 6.1 are very fresh releases. As such, please remember:

  * Not all extensions and themes have added support for the new versions!
  * You may experience issues if you have not pinned your documentation dependencies.
  * Issues may also be caused by new bugs in the Sphinx 6 compatibility of extensions and themes.
    Visiting the issue trackers of these projects is helpful.

* We are actively updating our theme to support Sphinx and docutils updates.
  If you find regressions in any new releases of the `sphinx-rtd-theme <https://sphinx-rtd-theme.readthedocs.io/>`_,
  please don't hesitate to `open an issue on GitHub <https://github.com/readthedocs/sphinx_rtd_theme/>`_.

If you suspect that upgrade issues are caused by dependency mismatches,
we recommend taking the approach of *reproducible builds*.
This includes explicitly specifying all relevant dependencies.
Read more in our documentation's :doc:`introduction to Reproducible Builds <readthedocs:guides/reproducible-builds>`.


Less maintenance work in the future
-----------------------------------

Sphinx 6 focuses on reducing the maintenance burden for the future.
This is done by simplifying the factor of supported docutils versions and Python versions.

Moving forwards,
the number of upgrade paths for documentation projects
are fewer and thus will lead to less choices for documentation owners and
maintainers of Sphinx themes and extensions.
This is a positive step forward for both documentation projects, themes and extensions.
If your Sphinx extensions and theme support Sphinx 6, we recommend this upgrade in order to reduce complexities and future technical debt.

.. _sphinx-rtd-theme: https://sphinx-rtd-theme.readthedocs.io/

