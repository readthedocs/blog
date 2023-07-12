.. post:: July 12, 2023
   :tags: builders
   :author: Manuel
   :location: BCN
   :category: Changelog

Doctools without configuration file (`conf.py` / `mkdocs.yml`) are deprecated
=============================================================================

Historically Read the Docs has created a `conf.py` file for Sphinx projects and a `mkdocs.yml` file for MkDocs projects that don't provide one,
to make onboarding easier. 
This has been confusing a lot our users in different ways and **we will remove the auto-creation of a default Sphinx/MkDocs configuration file for projects that don't have one on August 28th**. 
To avoid unexpected behavior or your documentation builds failing, 
you should add a configuration file to your project by this date.

The auto-creation of a default configuration file will be completely removed on **August 28th**. Add a `conf.py`/`mkdocs.yml` to your projects before this date to avoid unexpected build failures.

You can find a good example of a basic configuration file in our :doc:`example projects <readthedocs:examples>`:

* Sphinx `example conf.py <https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/docs/conf.py>`_
* Mkdocs `example mkdocs.yml <https://github.com/readthedocs-examples/example-mkdocs-basic/blob/main/mkdocs.yml>`_

Please `contact us`_ about any issues you have regarding change.

.. _contact us: mailto:hello@readthedocs.org

