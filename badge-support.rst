.. post:: Aug 14, 2014
   :tags: feature, badges

Badge Support
=============

Documentation is an often overlooked part of a software project.
Today we are releasing badges for your docs,
so that people can easily see that your docs are up-to-date.

Status Badges
-------------

The main use of badges is to show the status of your project's build.
They will display in green for passing,
red for failing,
and yellow for unknown states.

Here are a few examples:

|green| |nbsp| |red| |nbsp| |yellow|

You can see it in action in the `Read the Docs README`_.
They will link back to your project's documentation page on Read the Docs.

Project Pages
-------------

You will now see badges embedded in your `project page`_.
The default badge will be pointed at the *default version* you have specified for your project.
The badge URLs look like this::

	https://readthedocs.org/projects/pip/badge/?version=latest

You can replace the version argument with any version that you want to show a badge for.
If you click on the badge icon,
you will be given snippets for RST, Markdown, and HTML;
to make embedding it easier.

If you leave the version argument off,
it will default to your latest version.
This is probably best to include in your README,
since it will stay up to date with your Read the Docs project.

Design
------

We have often wondered what we might make our badges look like.
Luckily,
there is a developing standard and service to support badges.
http://shields.io is what we'll be using to generate our badges,
and they look beautiful.

Feature Requests
----------------

This is an initial attempt at adding badges to Read the Docs,
it's a feature we've wanted to add for some time.
We have some plans to improve badges further,
but be sure to get in touch with us if you have any feedback on how you would like to see badges used.

Feel free to `file an issue`_,
or you can always reach us at readthedocs@gmail.com.

.. _file an issue: https://github.com/rtfd/readthedocs.org/issues
.. _Read the Docs README: https://github.com/rtfd/readthedocs.org/blob/master/README.rst
.. _project page: https://readthedocs.org/projects/pip/
.. |green| image:: http://img.shields.io/badge/Docs-latest-green.svg
.. |red| image:: http://img.shields.io/badge/Docs-release--1.6-red.svg
.. |yellow| image:: http://img.shields.io/badge/Docs-No%20Builds-yellow.svg
.. |nbsp| unicode:: 0xA0 
   :trim:
