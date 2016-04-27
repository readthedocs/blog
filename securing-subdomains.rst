.. post:: Apr 27, 2016
   :tags: security
   :author: Anthony

Securing Subdomains
===================

Starting today, Read the Docs will start hosting projects from subdomains on
the domain ``readthedocs.io``, instead of on ``readthedocs.org``. This change
addresses some security concerns around site cookies while hosting user
generated data on the same domain as our dashboard.

Changes to provide security against broader threats have been in place for a
while, however there are still a few scenarios that can only be addressed by
migrating to a separate domain.

We implemented session hijacking detection and took precautions to limit cookie
usage, but there are still a number of scenarios utilizing XSS and CSRF attacks
that we aren't able to protect against while hosting documentation from
subdomains on the ``readthedocs.org`` domain. Moving documentation hosting to a
separate domain will provide more complete isolation between the two user
interfaces.

Projects will automatically be redirected, and this redirect will remain
in place for the foreseeable future. Still, you should plan on updating links to
your documentation after the new domain goes live.

If you notice any problems with the changes, feel free to open an issue on our
issue tracker: http://github.com/rtfd/readthedocs.org/issues. If you do notice
any security issues, contact us at security@readthedocs.org with more
information.

Keep on documenting,
The Read the Docs Team
