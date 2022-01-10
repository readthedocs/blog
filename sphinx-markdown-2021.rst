.. post:: Dec 20, 2021
   :tags: media, talk, conference, markdown, commonmark
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      During 2021 we have promoted the use of Markdown in Sphinx in various ways.
      In this post we show how you can start using it in your project today,
      and give some extra pointers.

Sphinx and Markdown around the world in 2021
============================================

Read the Docs has been committed to improving the accessibility
and user experience of Sphinx since the start,
and that includes the markup language in which the documentation is written.
Years ago, after carefully listening to users,
:doc:`we announced recommonmark </adding-markdown-support>`
to help bridging the immense popularity of Markdown
with the powerful capabilities of Sphinx.
(It is now deprecated in favor of MyST - keep reading to know more.)

It is no surprise that Markdown is in such demand:
thanks in large part to the huge popularity of GitHub,
`Markdown is nowadays the most widely used markup language in open-source
projects <https://passo.uno/docs-as-code-tools-open-standards/>`_,
ahead of reStructuredText, the second in the list, by an order of magnitude.

This year, thanks to the CZI Grant we received last year
and the effort of other communities,
especially `the Executable Book Project <https://executablebooks.org>`_,
we have devoted lots of resources to help consolidate Markdown
as a compelling markup language for Sphinx.

Writing Markdown in Sphinx
--------------------------

To that end, we recognized the potential of MyST as a successor of recommonmark,
and :doc:`deprecated the latter in favor of MyST-Parser </newsletter-april-2021>`.
To :doc:`start writing Markdown in Sphinx <sphinx:usage/markdown>`,
you need to follow three steps:

* Install ``MyST-Parser``: ``pip install myst-parser``

* Add ``myst_parser`` to the list of Sphinx extensions:

.. code-block:: python
   :emphasize-lines: 3

   extensions = [
       # ...other extensions
       "myst_parser",
   ]

* Start writing content in ``*.md`` files!

You can find more information in the :doc:`MyST-Parser documentation <myst-parser:index>`.

Talks and workshops at conferences
----------------------------------

Luckily the migration to MyST-Parser was trivial for most projects,
but we still wanted to spread the word about
the best practices for creating Sphinx projects on Read the Docs using MyST Markdown.
We set the goal of presenting at every large scientific Python event out there,
and all our proposals were accepted [1]_! Throughout 2021, we were present in several events:

- We conducted a networking session and a sprint about documentation
  at `SciPy US <https://www.scipy2021.scipy.org>`_,
  and in that event we were kindly invited to
  the `sktime documentation sprint <https://www.eventbrite.com/e/sktime-doc-sprint-tickets-164990684579>`_.
- We delivered a 90 minutes tutorial called
  `"Document your scientific project with Markdown, Sphinx, and Read the
  Docs" <https://pydata.org/global2021/schedule/presentation/17/document-your-scientific-project-with-markdown-sphinx-and-read-the-docs/>`_
  at PyData Global,
  and we repeated a 120 minute version in Spanish language
  at the `SciPy Latin America <https://conf.scipy.lat/en/>`_.
- And we also gave shorter talks at more broadly focused events:
  `PyCon Latam <https://www.pylatam.org/>`_ and `PyCon Spain <https://2021.es.pycon.org/>`_.

We have generated workshop material that everybody is welcome to use:

- A `main repository <https://github.com/readthedocs/tutorial-sphinx-markdown>`_
  containing some introductory slides about Sphinx,
  and detailed notes of every step of the tutorial.
- A `supporting repository <https://github.com/readthedocs/tutorial-sphinx-markdown-library/>`_
  with a tiny Python library that gets used during the tutorial,
  inspired by the one used in the :doc:`official Sphinx tutorial <sphinx:tutorial/index>`
  we authored with the help of the Sphinx community.

And finally, we have also developed an interactive web application to
`translate small bits of reStructuredText to MyST Markdown <https://mystyc.herokuapp.com/>`_.

.. [1] We also have submitted a proposal for SciPy India,
   which was postponed to January 2022.
   EuroSciPy and SciPy Japan didn't happen in 2021.

Future plans
------------

We are excited to see that the Executable Books team
has released `myst-docutils <https://pypi.org/project/myst-docutils/>`_,
which should help docutils parse CommonMark directly
and possibly pave the way for Sphinx to parse Markdown
without the need of third party extensions.
Hopefully that will also make it easier for Sphinx
to showcase Markdown content in its documentation more prominently,
and users will be able to naturally pick the markup language
that best suits their needs, be it reST or MyST.

---

Considering using Read the Docs for your next Sphinx, Jupyter Book, or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!
