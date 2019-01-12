.. post:: Jan 11, 2019
    :tags: deprecation
    :author: Anthony

Incoming Webhook Deprecations
=============================

In the coming weeks and months, Read the Docs will be moving some projects away
from our legacy incoming webhooks. About 2 years ago, these incoming webhooks
were replaced with project webhook integrations, at which point we improved
security and added several features to these incoming webhooks. New projects
have been using these integrations by default since, but it's possible that
your project is still using these deprecated incoming webhooks if your project
was configured on Read the Docs more than 2 years ago.

In order to continue building automatically, projects should reconfigure their
repository to use a new project webhook integration instead. For more
information, see our docs on :ref:`readthedocs:webhook-creation`.

There are two important dates to note here:

January 31st, 2019
    This is the date that GitHub will stop sending notifications through their
    GitHub Services. Your project might be relying on GitHub Services if your
    GitHub repository is using the ``ReadTheDocs`` GitHub Service and does not
    have another webhook to Read the Docs configured.

April 1st, 2019
    After this date, Read the Docs will stop accepting incoming webhook
    notifications for the remaining legacy incoming webhooks. You might be using
    one of these incoming webhooks if your repository has a webhook pointing to
    any of the following URLs:

    * https://readthedocs.org/build
    * https://readthedocs.org/bitbucket
    * https://readthedocs.org/github
    * https://readthedocs.org/gitlab

We will be sending periodic notifications over the next few weeks to the owners
of any projects that are still configured to use these deprecated incoming
webhooks.
