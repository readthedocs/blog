.. post:: November 28, 2023
   :tags: docs, versions
   :category: Changelog
   :author: Santos
   :location: CUE

Introducing versioning schemes
==============================

URLs are an important part of your documentation.
Users can infer from the URL if your documentation has or supports
multiple versions or translations.

Until now, Read the Docs allowed you to configure your project in two ways:

Multiple versions with translations
  Resulting in URLs like:

  - ``/en/latest/index.html``
  - ``/es/latest/index.html``
  - ``/en/1.0/index.html``

Single version without translations
  Resulting in URLs like:

  - ``/index.html``
  - ``/api/v3.html``

While not all projects have or require translations, many benefit from having multiple versions.
This meant that projects without translations but with need for multiple versions,
had to opt into supporting translations in order to have multiple versions.

We're excited to announce that we now support projects with multiple versions without translations.
Resulting in URLs like:

- ``/latest/index.html``
- ``/1.0/index.html``

Now instead of having a ``Single version`` checkbox in the ``Admin`` page of your project,
you'll see a ``Versioning scheme`` dropdown with three options available.

Changes in the API
------------------

In order to support this new feature, we have made some changes to the API.
Specifically, the ``single_version`` field has been deprecated in favor of the ``versioning_scheme`` field.

When updating a project, you should use the ``versioning_scheme`` field instead of the ``single_version`` field.
To avoid breaking existing integrations,
the ``single_version`` field will still be returned in the API,
but you should use the ``versioning_scheme`` field instead.
