.. post:: November 21, 2023
   :tags: docs, versions
   :category: Changelog
   :author: Santos
   :location: CUE

Introducing versioning schemes
==============================

URLs are an important part of your documentation.
Users can infer from the URL if your documentation has
multiple versions or translations.

Previously, Read the Docs allowed you to configure your project in two ways:

Multiple versions with translations
  Resulting in URLs like:

  - /en/latest/index.html
  - /es/latest/index.html
  - /en/1.0/index.html

Single version without translations
  Resulting in URLs like:

  - /index.html
  - /api/v3.html

Not all projects have translations or the need for them,
but many projects have the need for multiple versions.
This meant that projects without translations, but with multiple versions,
had to opt into the multiple versions with translations configuration in order to have multiple versions.

We are now introducing support for projects with multiple versions without translations,
resulting in URLs like:

- /latest/index.html
- /1.0/index.html

Now instead of having a ``Single version`` checkbox,
projects now will have a ``Versioning scheme`` dropdown with three options available.

Changes in API
--------------

In order to support this new feature, we have made some changes in the API.
Specifically, the ``single_version`` field has been deprecated in favor of the ``versioning_scheme`` field.

In order to avoid breaking existing integrations,
the ``single_version`` field will still be available in the API,
but you should use the ``versioning_scheme`` field instead.
