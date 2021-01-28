.. post:: Feb 1, 2021
   :tags: api, feature, reference
   :author: Manuel
   :location: BCN

API v3 is now stable!
=====================

We are excited to announce that our API v3 has reached its stable version,
and it's now available for all Read the Docs users.
This includes Read the Docs Community and Read the Docs for Business.
Since we :doc:`announced the beta version </api-v3-beta>` of it,
we have been adding extra functionality and bug-fixing some minor issues based on users feedback.

The new API v3 *is not* a fully replacement (yet!) of API v2,
but **we highly recommend using API v3 for all the new code you write from now on**.
API v2 is planned to be deprecated soon,
though we have not yet set a time frame for deprecation.
We will alert users with our plans when we do.


Nice features
-------------

These are some of the possible actions API v3 allows and we like the most,

- Ability to import new projects
- Activate a version
- Trigger builds
- Check build status
- Manage redirects

They allow you to easily manage common tasks like setup the documentation for a new project,
automate the release of a new version, or even pause it if you detect that the build failed for some reason.
Hook the rename of a file in your VCS to the creation of a redirect in its docs,
and more!

If you want to know more about it,
please check out the full `APIv3 documentation <https://docs.readthedocs.io/page/api/v3.html>`_.


Help us to make it better
-------------------------

We always love to hear from users about how they are using the API.
We want to help users to manage their projects' documentation in the easiest and less repetitive way possible.
Please, feel free to `open an issue in our issue tracker <https://github.com/rtfd/readthedocs.org/issues/>`_
if there is a use case we are not covering.
