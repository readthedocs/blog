.. post:: Jan 21, 2019
    :tags: deprecation
    :author: Anthony

Incoming Webhook Deprecations
=============================

In the coming weeks and months, Read the Docs will be moving some projects away
from our legacy incoming webhooks, towards our per-project webhook integrations.

Our legacy incoming webhooks were our first attempt at allowing providers like
GitHub to automatically trigger builds on for projects on Read the Docs. These
webhooks lacked a number of security features, and so, about two years ago, we
replaced these with per-project webhook integrations instead. We added a number
of features to per-project webhook integrations at the time, and we stopped new
projects from using the old incoming webhooks.

It's possible that your project is still using these deprecated incoming
webhooks if your project was configured on Read the Docs more than two years
ago. If your project does not have an webhook integrations under the
**Integrations** section of your project's admin dashboard, you might be using
these legacy incoming webhooks.

In order to continue building automatically, projects should reconfigure their
repository to use a new project webhook integration instead. For more
information, see our docs on :ref:`readthedocs:integrations:Integration Creation`.

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
