.. post:: Nov 11, 2021
   :tags: feature, jupyter
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Jupyter Book is now supported on Read the Docs,
      in this post we explain what is needed to make it work.

Read the Docs ❤️ Jupyter Book
=============================

We are proud to announce that now Jupyter Book projects are supported on Read the Docs!

Both Read the Docs and The Executable Book Project, the folks behind Jupyter Book,
share a common passion for documentation,
and we have been collaborating on various topics for some time already.
For example, we started promoting MyST in favor of our recommonmark
:doc:`back in April this year </newsletter-april-2021>`,
and we wrote a guide on :doc:`using Jupyter notebook with Sphinx <readthedocs:guides/jupyter>`
that benefitted a lot from their feedback.

Now we are happy to announce that Jupyter Book itself is supported on Read the Docs,
after some thorough discussion about the possible implementations
and thanks in large part to the Jupyter Book developers,
who addressed all the minor incompatibilities that prevented this from happening.

What is Jupyter Book?
---------------------

According to `its own documentation <https://jupyterbook.org/>`_,

   Jupyter Book is an open source project for building beautiful,
   publication-quality books and documents from computational material.

Jupyter Book is the flagship product of `the Executable Book Project <https://executablebooks.org/>`_,
an international collaboration between several universities and software projects
seeking to build open source tools
that facilitate publishing computational narratives
using the Jupyter ecosystem.

Even though Jupyter Book is much younger than Read the Docs as a project,
it has become very popular in recent times
among scientific software developers and educators.
It enables users to
write publication-quality content in Markdown thanks to MyST_
(a Markdown dialect compatible with Sphinx
:doc:`we started promoting back in April this year </newsletter-april-2021>`),
use Jupyter notebooks to author content thanks to `MyST-NB`_
(featured in our :doc:`Jupyter on Sphinx guide <readthedocs:guides/jupyter>`),
easily add interactivity thanks to Thebe_,
and much more.

.. _MyST: https://myst-parser.readthedocs.io/
.. _MyST-NB: https://myst-nb.readthedocs.io/
.. _Thebe: https://thebe.readthedocs.io

Why a change was needed
-----------------------

Read the Docs supports two documentation generation systems
Sphinx_ and MkDocs_.
Adding extra systems is difficult with the current codebase,
because it requires lots of effort to match all the features
currently supported by the existing ones.

On the other hand, even though `Jupyter Book leverages Sphinx "for almost everything that it
does" <https://jupyterbook.org/explain/sphinx.html#jupyter-book-is-a-distribution-of-sphinx>`_,
it purposefully hides some of the Sphinx implementation details from the user
to create a more user friendly experience.
One of the consequences of this is that
the assumptions that Read the Docs makes to build the documentation of Sphinx projects don't hold:
in particular, Jupyter Book uses a declarative configuration file ``_config.yml``
that gets translated on the fly to the Sphinx dynamic configuration usually stored in ``conf.py``.
As a result, Jupyter Book projects could not be hosted on Read the Docs - until now!

.. _Sphinx: https://www.sphinx-doc.org/
.. _MkDocs: https://www.mkdocs.org/

How to deploy a Jupyter Book project to Read the Docs
-----------------------------------------------------

With the current development version of Jupyter Book,
you can now export a Sphinx ``conf.py`` configuration
from the Jupyter Book declarative ``_config.yml``
and save it to disk,
which allows Read the Docs to build the documentation from it
like any other Sphinx project.

The challenge then becomes keeping both configuration files synchronized,
since every update to ``_config.yml`` or new Jupyter Book release
can potentially produce changes in the ``conf.py``.
As described in :doc:`the official documentation <jupyterbook:publish/readthedocs>`,
users can either :ref:`manually export the configuration <jupyterbook:sphinx:convert>`
running a command at will,
or :ref:`set up an automation to do it on every change <jupyterbook:sphinx:convert:pre-commit>`.

To see this in action, have a look at
`this example project <https://github.com/astrojuanlu/jupyterbook-on-read-the-docs>`_
that contains the bare minimum to make :doc:`the demo book <jupyterbook:start/create>`
work on Read the Docs.

We are excited that this is now possible
and look forward to seeing more projects built with Jupyter Book!

---

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!
