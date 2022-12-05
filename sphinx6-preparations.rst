.. post:: Dec 5, 2022
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Sphinx 6 is coming soon. Here are our thoughts about preparations that we
      are making, which may affect projects looking to upgrade.


Sphinx 6 is coming
==================

Sphinx 6 is not yet released, but it may be released before the arrival of our next newsletter.
Here are some of our considerations for getting ready for Sphinx 6:

- Sphinx 6 focuses on reducing the maintenance burden for the future,
  dropping support of docutils 0.14, 0.15, 0.16 and 0.17.
  This will make the work of theme and extension maintainers considerably easier,
  and we may start seeing themes requiring ``Sphinx>=6`` simply because it's less work to support.
- Sphinx 6 requires docutils 0.18 or 0.19.
  We are finalizing support for `sphinx-rtd-theme`_ which currently only supports docutils 0.17.
  These updates are almost finished and are planned to arrive in sphinx-rtd-theme 1.2.0.
- Sphinx 6 is removing jQuery, but we need it for `sphinx-rtd-theme`_.
  jQuery is easily added back using the new extension `sphinxcontrib-jquery`_.
- Sphinx 6 removes all bundled JavaScript libraries.
  If you depend on any of these,
  you may have to bundle them yourself or modify your implementation.
- See also the `Sphinx changelog <https://www.sphinx-doc.org/en/master/changes.html>`_

Since most documentation projects rely on themes and extensions, we recommend that you do not upgrade to Sphinx 6 before you see announcements of Sphinx 6 support in your themes and extensions.

.. _sphinx-rtd-theme: https://sphinx-rtd-theme.readthedocs.io/
.. _sphinxcontrib-jquery: https://pypi.org/project/sphinxcontrib.jquery/


