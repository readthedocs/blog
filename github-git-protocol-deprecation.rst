.. post:: February 15, 2022
   :tags: github, git, deprecation
   :author: Santos
   :location: CUE

Deprecation of the ``git://`` protocol on GitHub
================================================

Last year, GitHub announced_ the deprecation of the ``git`` protocol due to security reasons.
This change will be made permanent on March 15, 2022.

.. _announced: https://github.blog/2021-09-01-improving-git-protocol-security-github/

At Read the Docs we found around 900 projects using a URL of the form
``git://github.com/user/project`` to clone their projects.
To save time to our users, we have migrated those to use the ``https`` protocol instead,
this is ``https://github.com/user/project``.

But there are other places where users may be using a URL with the ``git`` protocol,
like in submodules or dependencies. You'll need to migrate those to use a supported
protocol in order for your builds to keep working after March 15, 2022.
In most cases, this means replacing the ``git://`` part with ``https://``,
if you have doubts, please check the documentation of the tools you are using,
for example:

- `git <https://git-scm.com/docs/git-submodule/#Documentation/git-submodule.txt-set-url--ltpathgtltnewurlgt>`__
- `pip <https://pip.pypa.io/en/stable/topics/vcs-support/#git>`__

**Note that this applies only to repositories hosted on GitHub**,
repositories using another provider that supports the ``git`` protocol won't be affected.
