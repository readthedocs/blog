.. post:: June 8, 2018
   :tags: privacy, advertising
   :author: David
   :location: SAN

Do Not Track at Read the Docs
=============================

Today, we are pleased to announce that Read the Docs honors `Do Not Track`_ (DNT).
DNT is a browser preference that requests that a user not be tracked
across the internet while browsing the web.

While there isn't a consensus on precisely what DNT should mean,
we are following the Electronic Frontier Foundation's (EFF) `guidelines`_
for Do Not Track as we believe that gives a good balance
between the privacy expectations of users and the reality of running a business
and keeping Read the Docs sustainable.

.. _Do Not Track: https://allaboutdnt.com/
.. _guidelines: https://www.eff.org/issues/do-not-track


What we implemented
-------------------

Not much needed to change to make Read the Docs support DNT
and many of these changes were already necessary
for the EU's new :doc:`privacy regulation </gdpr-what-it-means-for-readthedocs>`.

Here's a brief list of what we did for Do Not Track:

* Our logs that store any personal data are deleted after no more than ten days.
  We do this for all users even those who don't have DNT enabled.
* When a user has DNT enabled, we do not send data to our analytics.
  Based on our initial data, this looks like about a 6% reduction.
* While this didn't change, we reiterated that we **do not**
  do behavioral ad targeting regardless of DNT preference.
  
Full details on Do Not Track at Read the Docs can be found in our `privacy policy`_.

.. _privacy policy: https://docs.readthedocs.io/en/latest/privacy-policy.html#do-not-track


What DNT means for our advertising
----------------------------------

Advertising at Read the Docs was already built with privacy in mind.
With our :doc:`Ethical Ads <readthedocs:advertising/ethical-advertising>`, we previously committed to not tracking users,
not selling user data, and hosting ads ourselves
which all align perfectly with Do Not Track.

Our support for DNT formalizes our commitment to the high standards
for privacy produced by the EFF.
It also make us one of very few ad networks that honor Do Not Track.

The Ethical Ad Network
----------------------

In a :doc:`previous post </ethical-advertising-works>`,
we mentioned that we are taking the same developer-centric, privacy-focused
advertising we have on Read the Docs and expanding this to a larger ad network
for open source infrastructure.

Supporting Do Not Track is an important milestone along the way
as it confirms our commitment to privacy in advertising.
We believe that ads don't have to track people to be effective.

Our `Ethical Ad network`_ is still in its early stages,
but if you want to know more or you know a project that could use it, 
please `get in touch`_.

.. _Ethical Ad network: https://www.ethicalads.io/
.. _get in touch: mailto:ads@readthedocs.org
