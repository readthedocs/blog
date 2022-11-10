.. post:: December 14, 2021
   :tags: newsletter, python
   :author: Juan Luis
   :location: MAD

.. meta::
   :description lang=en:
      Company updates and new features from last month,
      current focus, and upcoming features in December.

Read the Docs newsletter - December 2021
========================================

Welcome to the latest edition of our monthly newsletter, where we
share the most relevant updates around Read the Docs,
offer a summary of new features we shipped
during the previous month,
and share what we'll be focusing on in the near future.

Company highlights
------------------

- We successfully deployed mitigation measures against spam,
  and we are happy to report that the amount of abusive projects
  has dramatically decreased.
- We started tracking usage of different parts of our application
  in a more systematic fashion which will enable us to make
  better product design decisions going forward.

New features
------------

- We revamped our support for :doc:`webhooks <readthedocs:build-notifications>`:
  now they have a dedicated section in the project settings,
  you can customize the payload,
  and you can inspect the status of each webhook delivery.
  Interested in receiving build notifications on :ref:`Slack <readthedocs:build-notifications:slack>`
  or :ref:`Discord <readthedocs:build-notifications:discord>`? Now you can!

.. figure:: /img/webhooks-events.png
   :align: center
   :width: 80%
   :alt: Revamped webhooks

   Revamped webhooks

- On Read the Docs for Business, we improved our security audit logs to show information from all the organization
  according to its plan.

.. figure:: /img/organization-audit-logs.png
   :align: center
   :width: 80%
   :alt: Organization audit logs

   Organization audit logs

- We expanded our documentation to describe :ref:`how document projects with Jupyter
  Book <readthedocs:faq:how can i deploy jupyter book projects on read the docs?>`
  and :doc:`how to use Poetry for dependency management <readthedocs:guides/poetry>`.

Thanks to our external contributor `Rok Roškar`_.

You can always see the latest changes to our platforms in our :doc:`Read the Docs
Changelog <readthedocs:changelog>`.

.. _Rok Roškar: https://github.com/rokroskar

Upcoming features
-----------------

With the Christmas holidays coming up, we will have a few slow weeks ahead.

- Ana_ will keep working on the complete redesign of our community site,
  which is already making good progress.
- Anthony_ will work with Ana_ on the structure of our new community site
  and document our upcoming new user interface.
- Eric_ will continue working on our commercial SSL provisioning and CDN with Santos_.
- `Juan Luis`_ will continue promoting our Embed API as well as wrap up
  his work on the Sphinx tutorial.
- Manuel_ will adjust the new logging and spam fighting systems,
  and continue making progress on the new metrics infrastructure.
- Santos_ will do the final bits of CDN work on our commercial site,
  finish moving our development documentation to a separate project,
  and continue unifying our commercial and community codebases.

Possible issues
---------------

Last week we accidentally banned a small number of legitimate users
and they saw their projects temporarily blocked.
As soon as we noticed this we apologized to the affected users
and rolled back the ban, and the documentation is now serving normally.

----

Considering using Read the Docs for your next Sphinx or MkDocs project?
Check out `our documentation <https://docs.readthedocs.io/>`_ to get started!

.. _Ana: https://github.com/nienn
.. _Anthony: https://github.com/agjohnson
.. _Eric: https://github.com/ericholscher
.. _Juan Luis: https://github.com/astrojuanlu
.. _Manuel: https://github.com/humitos
.. _Santos: https://github.com/stsewd
