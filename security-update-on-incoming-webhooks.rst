.. post:: November 14, 2023
   :tags: webhooks, integrations, security
   :category: Changelog
   :author: Santos
   :location: CUE

Security update on incoming webhooks from integrations
======================================================

Webhooks from integrations (like GitHub) are used to:

- Trigger builds when a new commit is pushed to a repository.
- Create and delete previews from pull requests (if you have this feature enabled).
- Update the identifier of the latest version (if you have your default branch set to empty in your project's settings).

Last week, our team was made aware that manually created webhooks from integrations lacked support for a shared secret,
which is used to verify the authenticity of the webhook,
ensuring they originate from the expected source and not from a malicious user.

In order to improve security, we have deployed an update so that all integrations are now created with a shared secret,
so we can verify the authenticity of the webhook.

Security implications
---------------------

The lack of a shared secret for manually created integrations together with a legacy feature that automatically created integrations in certain circumstances,
could have allowed unauthorized users to create integrations without a shared secret.
Allowing the attacker to trigger builds,
create and delete previews from pull requests (if you had this feature enabled),
and update the identifier of the latest version (if you had your default branch set to empty in your project's settings).

We published a `security advisory <https://github.com/readthedocs/readthedocs.org/security/advisories/GHSA-45hq-g76r-46wv>`__
with more details about this issue.

Action required
---------------

If you manually created a webhook integration for GitHub, GitLab or Bitbucket,
you may be affected by this issue.

We have updated some of the webhooks automatically for users that have an account connected to a Git provider,
for integrations that we weren't able to update automatically, we have contacted the owners of each project.
To check if you have integrations without a secret,
and to update them to include one, follow these steps:

- Go to your project's settings page.
- Click on the "Integrations" tab.
- Click on each integration, if the integration doesn't have a secret,
  you'll see a warning message.
- If you see the warning message,
  click on the "Resync webhook" button to generate a new secret.
- Follow the steps `from our documentation <https://docs.readthedocs.io/en/stable/guides/setup/git-repo-manual.html>`__ to update your provider's webhook with the new secret.

Deprecation of integrations without a secret
--------------------------------------------

In order to keep the builds of your projects working,
webhooks from integrations without a secret will continue working,
but with a limited functionality, they will only be able to trigger builds.

We strongly advise all users to update their integrations to include a secret as soon as possible.
Integrations without a secret are deprecated, and support for them will be removed on **January 31st, 2024**.
