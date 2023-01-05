.. post:: Jan 1, 2023
   :tags: newsletter, python
   :author: Ben
   :location: MLM

.. meta::
   :description lang=en:
      Company updates and new features from the last month,
      current focus, and upcoming features.

Read the Docs newsletter - January 2023
=======================================

Happy 2023!
In this newsletter,
we present the updates happening in 2022's last month and since the :doc:`previous newsletter </newsletter-december-2022>`.

.. Commenting out this stuff, isn't it better that 
.. 
.. News and updates
.. ----------------
.. 
.. Here are the latest updates from our team:

- 📹️ Eric delivered a talk at DjangoCon US 2022 about the state of art to document a project in 2022.
  You can watch it here: `Documenting Django Code in 2022`_
- 🛠️ We continued reorganizing our own documentation to follow the `Diátaxis Framework`_.
  We look forward to a "show and tell" about our experience refactoring them using this framework.
- 🚢️ Sphinx 6.0 and 6.1 have been released. Read :doc:`our considerations for upgrading </sphinx6-upgrade>`.
- 🔒️ We fixed a security vulnerability on our platform. See: `GHSA-368m-86q9-m99w`_

You can always see the latest changes to our platforms in our :doc:`Read the Docs Changelog <readthedocs:changelog>`.

.. _Documenting Django Code in 2022: https://www.youtube.com/watch?v=mqn0D4xat58
.. _Diátaxis Framework: https://diataxis.fr/
.. _GHSA-368m-86q9-m99w: https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-368m-86q9-m99w

Upcoming features
-----------------

- We're working on improving our integration with `Material for MkDocs <https://squidfunk.github.io/mkdocs-material/>`_, which is a great theme for `MkDocs <https://www.mkdocs.org/>`_ documentation projects.
- Many improvements to our URL handling code, which will allow us to support more flexible URL configurations for projects.
- A search redesign to make it nicer across our dashboard and in-doc search experiences. 
- 

Possible issues
---------------

Sphinx 6.0 and 6.1 were released very recently and you may experience issues if you upgrade or if you have not pinned your documentation dependencies.

We are actively updating our theme to support Sphinx and docutils updates.
If you find regressions in any new releases of the `sphinx-rtd-theme <https://sphinx-rtd-theme.readthedocs.io/>`_,
please don't hesitate to `open an issue on GitHub <https://github.com/readthedocs/sphinx_rtd_theme/>`_.


Tip of the month
----------------

TBD: Insert twitter embed

Awesome Project of the month
----------------------------

TBD: Insert twitter embed


Awesome Read the Docs Projects List 🕶️
--------------------------------------

Looking for more inspiration? Check out our new list: `Awesome Read the Docs Projects <https://github.com/readthedocs-examples/awesome-read-the-docs>`_.

----

Considering using Read the Docs for your next documentation project?

.. raw:: html

   <a href="https://docs.readthedocs.io/" style="background-color: #409cff; border-radius: 3px; color: #ffffff; display: block; margin: 30px auto; font-size: 18px; font-weight: 700; line-height: 24px; padding: 15px 0 15px 0; text-align: center; text-decoration: none; width: 238px;">
     Get started: Read our documentation
   </a>


Questions? Comments? Ideas for the next newsletter? `Contact us`_!

.. Keeping this here for now, in case we need to link to ourselves :)

.. _Contact us: mailto:hello@readthedocs.org
