.. post:: January 4th, 2022
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Sphinx 6 is out. Here are our thoughts about preparations that we
      are making, which may affect projects looking to upgrade.


Sphinx 6 is out and has important breaking changes
==================================================

Sphinx 6 was released on December 29, 2022.
It contains a few major breaking changes that users should be aware of,
and some smaller new features as well.
Here are some of our considerations for getting ready for Sphinx 6:

- Sphinx 6 requires Python 3.8+ and you will need to specify a Python version using the :ref:`readthedocs:config-file/v2:build.tools.python` setting.
- Sphinx 6 drops support of docutils 0.14, 0.15, 0.16 and 0.17.
- Sphinx 6 requires docutils 0.18 or 0.19.
  We are finalizing support for `sphinx-rtd-theme`_ which currently only supports docutils 0.17.
  These updates are almost finished and are planned to arrive in sphinx-rtd-theme 1.2.0,
  which you can already try out by installing ``sphinx-rtd-theme==1.2.0rc2``
  which supports docutils 0.18.
- Sphinx 6 is removing jQuery, but we need it for `sphinx-rtd-theme`_.
  jQuery is easily added back using the new extension `sphinxcontrib-jquery`_.
- Sphinx 6 removes all other bundled JavaScript libraries.
  If you depend on any of these,
  you may have to bundle them yourself or modify your implementation.
- See also the `Sphinx changelog <https://www.sphinx-doc.org/en/master/changes.html>`_

Since most documentation projects rely on themes and extensions, we recommend that you do not upgrade to Sphinx 6 before you see announcements of Sphinx 6 support in your themes and extensions.

.. _sphinxcontrib-jquery: https://pypi.org/project/sphinxcontrib.jquery/


Less maintenance work in the future
-----------------------------------

Sphinx 6 focuses on reducing the maintenance burden for the future.
This is done by simplifying the factor of supported docutils versions and Python versions.

Moving forwards,
the number of upgrade paths for documentation projects
are fewer and thus will lead to less choices for documentation owners and
maintainers of Sphinx themes and extensions.
At Read the Docs, we support both our main theme, `sphinx-rtd-theme`_, and a number of extensions for Sphinx.
In light of that,
we are direct beneficiaries of the reduced dependency matrix.

.. _sphinx-rtd-theme: https://sphinx-rtd-theme.readthedocs.io/

