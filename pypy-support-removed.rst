.. post:: July 10, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Support for PyPy3 removed
=========================

Starting on **July 18, 2023** PyPy3 will be removed as an option to build documentation on Read the Docs.

This feature was introduced as an alternative to make Sphinx build faster.
However, we found there are no projects building their documentation with PyPy3
and we decided to remove its support to simplify our product and reduce development maintanence.

Please, `contact us`_ and let us know if you *require* PyPy3 to build your documentation.

.. _contact us: mailto:hello@readthedocs.org
