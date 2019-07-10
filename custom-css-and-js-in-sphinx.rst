.. post:: July 10, 2019
   :tags: sphinx
   :author: David
   :location: SAN

.. meta::
   :description lang=en:
       Customize your documentation by adding CSS stylesheets or JavaScript files
       to change your docs' look and feel

Adding Custom CSS or JavaScript to Sphinx Documentation
=======================================================

In the Read the Docs documentation, we have a number of
`how-to guides`_
to help people solve specific problems with Sphinx and Read the Docs.
By far our most popular guide is on
`adding custom CSS and JavaScript to Sphinx`_.

In some older versions of Sphinx, this process was a little more challenging
and it wasn't as easy to figure out how to do it from the Sphinx docs.
Sphinx 1.8 really streamlined this process especially for the simple cases.

.. _how-to guides: https://docs.readthedocs.io/page/guides/index.html
.. _adding custom CSS and JavaScript to Sphinx: https://docs.readthedocs.io/page/guides/adding-custom-css.html


Adding additional stylesheets or scripts
----------------------------------------

If your custom stylesheet is ``_static/css/custom.css``,
you can add that CSS file to the documentation using the
Sphinx option `html_css_files`_:

.. code-block:: python

    ## conf.py

    # These folders are copied to the documentation's HTML output
    html_static_path = ['_static']

    # These paths are either relative to html_static_path
    # or fully qualified paths (eg. https://...)
    html_css_files = [
        'css/custom.css',
    ]


A similar approach can be used to add JavaScript files:

.. code-block:: python

    html_js_files = [
        'js/custom.js',
    ]


That's it!
You don't need to create a Sphinx extension anymore to add a bit of custom CSS or JavaScript.

.. _html_css_files: https://www.sphinx-doc.org/page/usage/configuration.html#confval-html_css_files


Customizations supported by your theme
--------------------------------------

I should also note that depending on the theme you're using and what you're hoping to accomplish,
you may not even need to add custom CSS or JavaScript.
Many themes support a number of "theme options"
for customizing their look and feel without having to write custom code.
For example, here are all the options for the `Read the Docs theme`_ and the `Alabaster theme`_
which are the two most popular themes on Read the Docs itself.

.. _Read the Docs theme: https://sphinx-rtd-theme.readthedocs.io/page/configuring.html
.. _Alabaster theme: https://alabaster.readthedocs.io/page/customization.html

Both themes, for example, support the addition of Google Analytics to documentation by setting the ``analytics_id`` option:

.. code-block:: python

    ## conf.py

    html_theme_options = {
        'analytics_id': 'UA-XXXXXXX-1',  #  Provided in your GA dashboard
    }


In summary
----------

To recap, it only takes a few additions to your ``conf.py`` to add custom CSS or JavaScript.
However, it's also worth taking a look at your theme's docs or `Sphinx's built-in HTML options`_
to see if what you're trying to do is already supported.

Happy documenting!


.. _Sphinx's built-in HTML options: https://www.sphinx-doc.org/page/usage/configuration.html#options-for-html-output
