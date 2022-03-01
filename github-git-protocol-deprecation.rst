.. post:: March 1, 2022
   :tags: github, git, deprecation
   :author: Santos
   :location: CUE

Deprecation of the ``git://`` protocol on GitHub
================================================

Last year, GitHub announced_ the deprecation of the unsecured Git protocol due to security reasons.
This change will be made permanent on March 15, 2022.

.. _announced: https://github.blog/2021-09-01-improving-git-protocol-security-github/

At Read the Docs we found around 900 projects using a Git protocol URL
(``git://github.com/user/project``) to clone their projects.
To save time for our users, we have migrated those to use the HTTPS cloning URL instead
(``https://github.com/user/project``).

But there are other places where projects may be using a Git protocol URL,
like in submodules or dependencies. You'll need to migrate those to use a supported
protocol in order for your builds to keep working after March 15, 2022.
In most cases, this means changing URLs that start with ``git://`` to start with ``https://`` instead.
If you have doubts, please check the documentation of the tools you are using,
for example:

- `Git submodule URLs <https://git-scm.com/docs/git-submodule/#Documentation/git-submodule.txt-set-url--ltpathgtltnewurlgt>`__
- `Pip VCS support <https://pip.pypa.io/en/stable/topics/vcs-support/#git>`__

**Note that this applies only to repositories hosted on GitHub**,
repositories using providers that support the Git protocol won't be affected.

Read the Docs tries to keep users informed about deprecations
and breaking changes that may impact projects.
To receive future updates like this, `subscribe to our newsletter <https://landing.mailerlite.com/webforms/landing/p8b7z2>`__.
