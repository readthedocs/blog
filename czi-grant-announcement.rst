.. post:: Nov 19, 2020
   :tags: czi, grant, czi-grant,
   :author: Eric

Announcing Chan Zuckerberg Initiative Grant to Expand the Interoperability of Scientific Documentation
======================================================================================================

We're excited to announce that `Read the Docs`_ has received a $200,000 grant from the Chan Zuckerberg Initiative's `Essential Open Source for Science`_ (EOSS) program.
Read the Docs is the largest open source documentation hosting platform in the world.
We provide hosting for many scientific software packages,
including some that have received EOSS funding in the past.
You can read more about this round of grants in the `official announcement <https://cziscience.medium.com/scaling-open-infrastructure-and-reproducibility-in-biomedicine-69546a399747>`_.

Our grant has two parts:

* Part 1 allows us to develop new software to improve the interoperability of scientific documentation.
* Part 2 allows us do advocacy work around the importance and value of documentation in the scientific community.

We're excited about the chance to work with the scientific community to improve the overall experience of writing and reading documentation.
We plan to do a lot of outreach to various community members,
so that we can ensure we're building tools that provide the most value.
We also plan to write content that will hopefully make the process of documenting scientific code easier.

.. _Read the Docs: https://readthedocs.org/
.. _Essential Open Source for Science: https://chanzuckerberg.com/rfa/essential-open-source-software-for-science/

Part 1: improve the interoperability of scientific documentation
----------------------------------------------------------------

This work is something that we've been doing as a side project for some time now.
We have an extension to Sphinx that we call `sphinx-hoverxref`_.
It provides hovering tooltips for Sphinx projects when hover over a link.
You might be familiar with this functionality on GitHub or Wikipedia -- this project adds that functionality to any project hosted on Read the Docs.
You can see a `live demo <https://cpython-ericholscher.readthedocs.io/en/sphinx-hoverxref/whatsnew/3.9.html>`_ on a fork of the Python documentation.

The goal of the grant will be to expand this functionality by doing a few things:

* Improving and documenting the backend Embed API on Read the Docs, allowing documentation content to be embedded anywhere on the web.
* Building a JavaScript client for the Embed API, which includes tooltips showing the content on any website.
* Integrating this JS client and backend API together in a new version of sphinx-hoverxref.
* Extending sphinx-hoverxref to work across multiple Read the Docs sites, allowing content hovers across the entire scientific documentation ecosystem.
* If time allows, also extending the backend Embed API to support Sphinx documentation hosted outside of Read the Docs, allowing even more interoperability between documentation.

We are planning to contract a frontend developer to help with this work.
The Python work will likely be carried out by our existing team,
funded via the grant.
This is because of the complexities involved with the Read the Docs and Sphinx integration,
it will be more cost effective to have people already familiar with the codebases on these tasks.

.. _sphinx-hoverxref: https://github.com/readthedocs/sphinx-hoverxref

Part 2: Advocacy work around documentation in the scientific community
----------------------------------------------------------------------

We know that documentation is a pain point for scientific projects. There is a lack of resources in the community, and we feel that we can be a central clearing house for better documentation tutorials and best practices. This part of the funding will be about growing appreciation and knowledge of documentation in the scientific community in general, and advocating for time to be spent on crafting good documentation with the best tooling.

Part of this work would be letting people know about the work in Part 1, promoting the tooling to make better documentation in the Scientific Python ecosystem. Beyond that, we will also promote tutorials and best practices around documentation for Scientific users, leading to more resources being available and better documentation in the community.

The high-level roadmap for this part of the grant is:

* Improve documentation and promote the work in Part 1.
* Adapt the `Guides <https://docs.readthedocs.io/en/latest/guides/>`_ section of the Read the Docs documentation into a more full-featured Education section, along with standardizing and editing all existing guides.
* Expand our existing `Sphinx Tutorial <https://sphinx-tutorial.readthedocs.io/>`_, hopefully adding it upstream to Sphinx as the official tutorial
* Write additional documentation guides focused on the scientific community, based on feedback from people in the community. This will likely include tutorials on integrating Jupyter with Sphinx, `Jupyterbook <https://jupyterbook.org/intro.html>`_, and other pain points that users have.
* If time allows, we would also love to work on curating some of the documentation resources at `Write the Docs <https://www.writethedocs.org/topics/>`_, specifically topics that are relevant to scientific projects.

As part of this work, we plan to contract someone in a technical writer/developer evangelist role.
Someone with knowledge of the scientific community would be a great benefit,
given that we plan to seek feedback from many scientific projects on the priority of tasks we work on.

Looking forward
---------------

We are starting to look for contractors who would be a good fit for the work.
People who care about documentation and are already connected with the scientific community are a big plus.
We hope to post proper job descriptions for these roles in the near future,
but wanted to note that we're looking in our initial announcement.

This is the largest grant that we've ever received,
and we are working hard to make sure it's successful.
We appreciate the trust that the Chan Zuckerberg Initiative has placed in us,
and we will work hard to make sure the results of this grant will be adopted across the scientific ecosystem.

If you want to keep up to date with this work,
you can follow along on `GitHub <http://github.com/readthedocs/>`_ or `subscribe <#mc_embed_signup_scroll>`_ to our blog for updates.
