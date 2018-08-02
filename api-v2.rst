.. post:: August 2, 2018
   :tags: api, feature, reference
   :author: David
   :location: SAN

Read the Docs Public API
========================

Recently, we revamped Read the Docs' public API.
Previously, our latest API (v2) was used by our build processes
but not heavily used by outside users.

As part of this process, we put effort into making sure the API is easy to use
to access Read the Docs *projects*, *builds*, and *versions*,
easier to filter builds and versions by a particular project,
and that the `documentation`_ is up-to-date.

.. _documentation: https://docs.readthedocs.io/en/latest/api/v2.html


Deprecation of API v1 and connecting over insecure HTTP
-------------------------------------------------------

As part of this process, we are formally deprecating support for our `API v1`_.
It will be **supported through at least January 1, 2019**
but we strongly encourage all users to migrate to API v2 at their earliest convenience.

In addition, both API v1 and API v2 allowed connecting over insecure HTTP
as opposed to HTTPS. **Beginning in January 2019, we will be redirecting requests over HTTP to HTTPS.**
This will improve security and allow us to add more security related features to the API going forward.
For most users, this should be a one line change to connect to the HTTPS version of the API.

.. _API v1: https://docs.readthedocs.io/en/latest/api/v1.html


Get in touch
------------

We are always interested in the amazing things people create when data is openly shared.
In addition, we are always looking in improve our API to enable more projects and mashups.
If you use Read the Docs' public API for your project
or there are additional features you'd like to see in it,
we would love to `hear from you`_.

.. _hear from you: mailto:team@readthedocs.org
