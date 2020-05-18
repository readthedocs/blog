.. post:: May 18, 2020
   :tags: community, cdn, hosting
   :author: Eric

.. meta::
   :description lang=en:

      Read the Docs Community now has Cloudflare CDN enabled for all projects resulting in faster and more secure documentation worldwide.


Shipping a CDN on Read the Docs Community
=========================================

You might have noticed that our Read the Docs Community site has gotten faster in the past few weeks.
How much faster likely depends on how far away you live from Virginia,
which is where our servers have traditionally lived.

We have recently enabled a CDN on **all Read the Docs Community sites**,
generously sponsored by `CloudFlare`_.
This post will talk a bit more about how we implemented this,
and why we're excited about it.

We are also offering the CDN option to our Read the Docs for Business users on the Enterprise plan,
you can `reach out`_ to us if you're interested. 

Hosting thousands of domains is hard
------------------------------------

Traditionally the largest problem that we've had with rolling out features to all of our documentation sites is scale.
We host thousands of custom domains for our users,
and any solution needs to work across all of them.
This has presented a number of issues in the past,
but CDN is one of the most complicated.

To make a CDN function across all our sites,
every data center that the CDN has needs to work with all our custom domains.
Imagine we have 5,000 domains and there are 100 data centers across the world,
this means that ``5,000 * 100 = 500,000`` different endpoints need to be configured for this to work at scale.

We are lucky that CloudFlare has the global scale to be able to donate us this service.
Specifically,
their `SSL for SAAS`_ service is what we're using for both SSL and CDN across all our custom domains.
This allows us to offload the complexity to CloudFlare,
and only focus on our integration.

Implementation
--------------

One of the coolest things that CloudFlare's CDN offers is something called `Cache Tags`_.
This lets us add a ``Cache-Tag`` header to all the documentation that we serve,
and invalidate the cache using just that tag.

An example,
when you load our docs,
we will return a header::

    GET https://docs.readthedocs.io/en/latest/
    ...
    Cache-Tag: docs,docs-latest

We return a tag that matches both the ``$project``, and the ``$project-$version``.
This allows us to invalidate the cache for a specific version,
or across the entire project.

As you know,
cache invalidation is one of the harder problems,
so we take a pretty conservative approach.
We invalidate the cache in the following scenarios:

* Project cache on Project or Domain save
* Version cache on documentation builds for specific versions

The client code is quite simple,
a single HTTP request to Cloudflare's API with a list of ``tags`` to clear.

Outcomes
--------

There are two important outcomes from this work:

* Page loads are much faster for users around the world
* Our server load has gone down quite a lot because we handle fewer requests

The biggest winner here is our users.
Docs are faster for everyone,
and we are looking at implementing additional features into our documentation hosting code now that we have reduced load.

We hope that Read the Docs Community has gotten noticeably faster,
and that in the near future it will continue to get better with the new features that this enables.

.. _CloudFlare: https://www.cloudflare.com/ 
.. _reach out: mailto:support@readthedocs.org
.. _SSL for SAAS: https://www.cloudflare.com/ssl-for-saas-providers/
.. _cache tags: https://support.cloudflare.com/hc/en-us/articles/200169246-Purging-cached-resources-from-Cloudflare#h_6d756ac9-c476-45e8-a5d4-e2a6e45d9dc7

