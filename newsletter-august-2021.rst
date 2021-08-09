.. post:: August 9, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features in August.

Read the Docs newsletter - August 2021
======================================

Welcome to the latest edition of our monthly newsletter, where we
share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

- We have a new team member! Ana_ just joined us as Frontend Developer
  in the context of :doc:`the CZI grant we were awarded </czi-grant-announcement/>`
  to work on our JavaScript documentation embedding client
  and the Read the Docs redesign and UX.
- The first version of `the tutorial we contributed to the official
  Sphinx documentation <https://www.sphinx-doc.org/en/master/tutorial/>`_ is online,
  as part of the new Sphinx 4.1 releases, and we are already working on expanding it.
  We thank the Sphinx maintainers for the thorough reviews
  and CZI for making it possible.
- `We are now tracking changes in our
  database <https://github.com/readthedocs/readthedocs.org/pull/8355/>`_,
  which will help us with support issues and additional auditing features on Read the Docs for Business.

New features
------------

- We added support for Python 3.10b4 in our ``testing`` Docker images!
  `The final 3.10.0 release will be in October <https://www.python.org/dev/peps/pep-0619/>`_,
  but you can already test a development version.
- Our commercial site `now allows pull request previews to be public rather than private
  only <https://docs.readthedocs.io/en/stable/versions.html#privacy-levels>`_,
  and `to control the privacy level of pull request
  builds <https://docs.readthedocs.io/en/stable/pull-requests.html#privacy-levels>`_
  as well. As a result, we have dropped privacy levels for projects on our community site,
  since they used to be a source of confusion.
- We released `sphinx-hoverxref 0.7b1 <https://pypi.org/project/sphinx-hoverxref/0.7b1/>`_,
  which adds compatibility with Sphinx 4.1.
- We fixed a long-standing usability issue in both our community and commercial sites:
  notifications now have a close button.

.. figure:: /img/close-notifications-org.png
   :align: center
   :width: 80%
   :alt: Button to close notifications
  
   Button to close notifications

You can always see the latest changes to our platforms in our `Read the Docs
Changelog <https://docs.readthedocs.io/page/changelog.html>`_.

Upcoming features
-----------------

- Ana_, our new hire, will spend some time getting familiarized with our
  development practices and tools, and perform some quality assurance on
  `the upcoming new version of our Sphinx
  theme <https://github.com/readthedocs/sphinx_rtd_theme/milestone/6>`_
  along with Anthony_.
- Anthony_ will work on onboarding Ana_, release a first release candidate
  of version 1.0 of our Sphinx theme, and some finance work.
- Eric_ will continue overseeing the implementation of the next stages of
  our audit tracking along with Santos_, doing code review, and improving
  our sales & marketing processes.
- `Juan Luis`_ will expand the Sphinx tutorial while doing basic
  bug triaging for the project, and start with a much needed tutorial for
  Read the Docs itself. 
- Manuel_ will keep working on our Embed API version 3, push the final
  tweaks needed to support Python 3.10 along with Santos_,
  and continue improving our deployment processes.
- Santos_ will continue with the implementation of our audit tracking,
  inform our users about the upcoming changes in privacy levels on our
  community site, and wrap up the work around sharing specific
  versions of commercial projects.

Possible issues
---------------

Projects that were using Git LFS on our site noticed that `it stopped working
at the end of June <https://github.com/readthedocs/readthedocs.org/issues/8288>`_.
Even though it is not officially supported from our side,
we wanted to make it work again,
but it took several days to understand what was happening.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Ana: https://github.com/nienn
.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
