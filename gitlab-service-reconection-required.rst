.. post:: Sep 14, 2022
   :tags: gitlab
   :author: Santos
   :location: CUE

GitLab service re-connection required
=====================================

Some `months ago`_ GitLab started enforcing an expiration time of two hours for all of their OAuth tokens.

.. _months ago: https://gitlab.com/gitlab-org/gitlab/-/blob/master/CHANGELOG.md#1500-2022-05-20

Unfortunately `this broke`_ the integration with our application,
so your OAuth tokens may have expired.
OAuth tokens are used to interact with the GitLab API,
for reporting the status of merge requests, creating webhooks, and listing repositories.
In order for Read the Docs to have access to new fresh tokens,
you need to re-connect your GitLab account.
You can do this by clicking the `Login with GitLab` button on the Read the Docs login page.

We apologize for any inconvenience caused.

.. _this broke: https://github.com/readthedocs/readthedocs.org/pull/9594
