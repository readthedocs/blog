.. post:: August 13, 2018
   :tags: security, feature
   :author: David
   :location: SAN


HTTPS for Custom Domains
========================

Read the Docs hosts documentation for over 80,000 open source projects
and over 2,500 of those projects are hosted on their own individual domains.
Documentation hosted on ``*.readthedocs.io`` has supported HTTPS for a number of years,
but one of our most requested features was to make HTTPS on other domains easy.
Today we are happy to announce that **Read the Docs supports HTTPS on custom domains**!

Earlier this year, Cloudflare contacted us to support HTTPS
for the thousands of open source documentation projects on their own domains.
They generously provided us with their `SSL for SaaS`_ package
to ease the integration on our side.

.. _SSL for Saas: https://www.cloudflare.com/ssl-for-saas-providers/


Why HTTPS is important
----------------------

HTTPS encrypts traffic between your computer and Read the Docs' servers
and allows your browser to verify that the website you are talking to
is the one that you requested.
HTTPS ensures there is no man-in-the-middle snooping on your connection.


Configuring your domain
-----------------------

If you followed our `documentation for custom domains`_
and you are using a ``CNAME`` to point to Read the Docs,
no action is required on your part.

If you have had your Read the Docs setup for many years you may have followed some old directions
that suggested creating a ``CNAME`` to ``readthedocs.org`` or ``<slug>.readthedocs.org``.
Depending on your setup, we may not have been able to issue a certificate for your domain.
In that case, update your ``CNAME`` to point to ``readthedocs.io``.

.. _documentation for custom domains: https://docs.readthedocs.io/en/latest/alternate_domains.html


Why did it take so long?
------------------------

It's 2018! HTTPS is supposed to be easy, right?
For a few domains, getting a certificate isn't too hard.
For 2,500+ domains, things get a bit more complicated.

We identified a number of challenges including:

- Retrying failed requests to issue certificates
- Handling when users remove DNS records that would allow us to issue certificates
- Getting our web servers and load balancers to handle dynamically adding and updating certificates on the fly
- Handling recurring tasks to re-issue updated certificates before they expire

Cloudflare reduced most of this complexity to a few API calls made when a new domain is configured or removed.
Without their support, we would still be working on this feature.


Next steps
----------

There are a few more things left on our road map for this feature.
In the next few weeks we will begin to generate HTTPS links for custom domains where we have a certificate. 
After that change has been deployed for a few weeks, we will begin to redirect custom domain traffic to HTTPS.

As always, if you're having any trouble with a particular domain,
don't hesitate to let us know in our `issue tracker`_.

.. _issue tracker: https://github.com/rtfd/readthedocs.org/issues
