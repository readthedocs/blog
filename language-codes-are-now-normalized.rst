.. post:: October 24, 2023
   :tags: docs, languages, translations
   :category: Changelog
   :author: Santos
   :location: CUE

Language codes are now normalized
=================================

The following language codes are now normalized to be lowercase and use a dash as a separator instead of an underscore:

- ``nb_NO`` is now ``nb-no``
- ``pt_BR`` is now ``pt-br``
- ``es_MX`` is now ``es-mx``
- ``uk_UA`` is now ``uk-ua``
- ``zh_CN`` is now ``zh-cn``
- ``zh_TW`` is now ``zh-tw``

This change affects the following areas:

API:
   - When creating or updating projects, you must now use the new normalized language codes.
   - The API responses will include the new normalized language codes.

Docs and download URLs:
   Previous URLs from projects using the old language codes will redirect to the new normalized language codes.
   For example:

   - ``https://docs.readthedocs/pt_BR/latest/`` will redirect to ``https://docs.readthedocs/pt-br/latest/``.
   - ``https://docs.readthedocs/_/downloads/pt_BR/latest/pdf/`` will redirect to ``https://docs.readthedocs/_/downloads/pt-br/latest/pdf/``.

This change was implemented to ensure more `readable and clean URLs <https://en.wikipedia.org/wiki/Clean_URL>`__.
