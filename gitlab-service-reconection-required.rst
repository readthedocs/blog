.. post:: Sep 14, 2022
   :tags: gitlab
   :author: Santos
   :location: CUE

GitLab service re-connection required
=====================================

Some `months ago`_ GitLab started enforcing an expiration time of two hours for all of their OAuth tokens.

.. _months ago: https://gitlab.com/gitlab-org/gitlab/-/blob/master/CHANGELOG.md#1500-2022-05-20

Unfortunately, our application `wasn't ready`__ to handle this change,
so your OAuth tokens may have expired.
OAuth tokens are used to interact with the GitLab API,
for reporting the status of merge requests, creating webhooks, listing repositories etc.
In order for Read the Docs to have access to new fresh tokens,
you need to re-connect your GitLab account,
you can do this at https://readthedocs.org/accounts/gitlab/login/?process=connect,
or by going to https://readthedocs.org/accounts/social/connections/ and click on ``Connect to GitLab``.

We apologize for any inconvenience caused.

.. _wasn't ready: https://github.com/readthedocs/readthedocs.org/pull/9594
