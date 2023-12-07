.. post:: January 2, 2024
   :tags: redirects, docs
   :category: Changelog
   :author: Santos
   :location: CUE

New improvements to redirects
=============================

As your documentation evolves, content is moved, and pages are renamed,
leading to broken links for your users.
Redirects allow you to point users to the new location of a page.

We are excited to announce significant improvements to our redirects feature to make them more flexible and powerful.

Key improvements
----------------

HTTP status code
  You can now choose the `HTTP status code`_ for your redirects,
  selecting between 301 (permanent redirect) and 302 (temporary redirect).
  Previously, all redirects had the status code 302.

.. _HTTP status code: https://developer.mozilla.org/en-US/docs/Web/HTTP/Redirections

Explicit ordering
  Redirects now have an explicit order,
  allowing you to control the order in which they are processed.
  Previously, redirects were ordered based on their last modification date.

Disable redirects without deletion
   You can now disable redirects without deleting them.
   This is useful when debugging or when you want to temporarily disable a redirect.

Trailing slash
  Redirects now apply to URLs with and without a trailing slash.
  Previously, you had to create two redirects to handle both cases.

Suffix wildcards
  While we already supported suffix wildcard redirects, their functionality was limited.
  Now wildcard redirects use a more familiar syntax, ``*`` instead of ``$rest``,
  and the ``:splat`` placeholder is available in the target URL.
  Wildcards can be used with *Exact* and *Page* redirects.

Other changes
-------------

- Redirects aren't processed in domains from pull requests previews.
  You should treat these domains as ephemeral and not rely on them for user-facing content.
- Redirects now have a description field, allowing you to provide additional information about the redirect.
- *Sphinx HTMLDir -> HTML* and *Sphinx HTML -> HTMLDir** redirects where renamed to *Clean URL to HTML* and *HTML to Clean URL* redirects.
  These types of redirects are valid for all documentation tools, not just Sphinx.
- Prefix redirects were removed.
  The same functionality can be achieved with an *Exact* redirect using a wildcard.

For more details and examples, refer to `our documentation`_.

.. _our documentation: https://docs.readthedocs.io/en/stable/user-defined-redirects.html#user-defined-redirects

Breaking changes
----------------

In order to support these new improvements, we have made some breaking changes:

- The old ``$rest`` syntax for wildcard redirects is no longer supported.
  Use ``*`` instead.
- When using a wildcard, the matched suffix is no longer added to the target URL automatically.
  Use the ``:splat`` placeholder in the target URL to add the matched suffix.
- The redirect type ``sphinx_html`` used in the API was renamed to ``clean_url_to_html``.
- The redirect type ``sphinx_htmldir`` used in the API was renamed to ``html_to_clean_url``.
- The prefix redirect type was removed.
  Use an *Exact* redirect with a wildcard instead.

If you had redirects using the old syntax, you don't need to do anything.
We have automatically migrated them to use the new syntax.
