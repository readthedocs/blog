.. post:: Aug 22, 2014
   :tags: feature, redirects, migrating, new-user

User-defined Redirects
======================

Today we are announcing User-defined Redirects for Read the Docs.
This has been a long requested feature that should cut down on 404's when migrating your documentation.

Read the Docs has long had `Redirects`_,
but they are managed automatically for only certain use cases.
This change allows users to control a specific set of common redirects.

Prefix Redirects
----------------

The most useful and requested application of redirects was to migrate to Read the Docs from an old host.
You would have your docs served at a previous URL,
but that URL would break once you moved them.
Read the Docs includes a language and version slug in your documentation,
but not all documentation is hosted this way.

Say that you previously had your docs hosted at ``http://docs.example.com/dev/``,
and you move ``docs.example.com`` to point at Read the Docs.
Users will have a bookmark saved to a page at ``http://docs.example.com/dev/install.html``,
a URL that no longer exists.

You can now set a *Prefix Redirect* that will redirect all 404's with a prefix to a new place.
The example configuration would be::

    Type: Prefix Redirect
    From URL: /dev/

Your user's query would now redirect in the following manner::

	docs.example.com/dev/install.html ->
	docs.example.com/en/latest/install.html

Where ``en`` and ``latest`` are the default language and version values for your project.

Page Redirects
--------------

A more specific case is when you move a page around in your docs.
The old page will start 404'ing,
and your users will be confused.
*Page Redirects* let you redirect a specific page.

Say you move the ``example.html`` page into a subdirectory of examples: ``examples/intro.html``.
You would set the following configuration::

    Type: Page Redirect
    From URL: example.html
    To URL: examples/intro.html

Sphinx Redirects
----------------

We also support redirects for changing the type of documentation Sphinx is building.
If you switch between *HTMLDir* and *HTML*, your URL's will change.
A page at ``/en/latest/install.html`` will be served at ``/en/latest/install/``,
or vice versa.
The built in redirects for this will handle redirecting users appropriately.

Implementation
--------------

Since we serve documentation in a highly available way,
we do not run any logic when we're serving documentation.
This means that redirects will only happen in the case of a *404 File Not Found*.

In the future we might implement redirect logic in Javascript,
but this first version is only implemented in the 404 handlers.


Feature Requests
----------------

This is an initial attempt at redirects.
We have some plans to improve this,
but get in touch with us if you have ideas for improving the feature.

Feel free to `file an issue`_,
or you can always reach us at readthedocs@gmail.com.

.. _`file an issue`: http://github.com/rtfd/readthedocs.org/issues
.. _Redirects: http://docs.readthedocs.org/en/latest/redirects.html
