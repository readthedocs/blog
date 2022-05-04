.. post:: May 5, 2022
   :tags: announcement, feature, builds
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      We released user-defined build jobs (``build.jobs`` config key)
      which will help you with your custom build process!


Announcing user-defined build jobs
==================================

We are happy to announce a new feature to specify user-defined build jobs on Read the Docs.
If your project requires custom commands to be run in the middle of the build process,
they can now be executed with the new config key ``build.jobs``.
This opens up a complete world full of new and exciting possibilities to our users.


Background about the build process
----------------------------------

If your project has ever required a custom command to run during the build process,
you probably wished you could easily specify this.
You might have used a hacky solution inside your Sphinx's ``conf.py`` file,
but this was not a great solution to this problem.

That solution wasn't support,
and it had another important limitation: it only ran the commands *from inside* Sphinx's build command.
It was impossible to run a command after cloning the repository,
or before starting the Sphinx build process.
With the addition of the new config key ``build.jobs``,
you can do these things and more!

Using ``build.jobs`` in your configuration file
-----------------------------------------------

`Read the Docs' build process <https://docs.readthedocs.io/en/stable/builds.html>`_ is well-defined and divided into these pre-defined jobs:
``checkout``, ``system_dependencies``, ``create_environment``, ``install``, ``build`` and ``upload``.
Now, with the introduction of ``build.jobs``, you can hook these with custom commands that run before & after.

Let's say your project requires to run a command immediately *after* clonning the repository in the ``checkout`` job.
In that case, you will want to use the ``build.jobs.post_checkout`` config key:

.. code:: yaml
   :caption: .readthedocs.yaml
   :emphasize-lines: 6-10

    version: 2
    build:
      os: ubuntu-22.04
      tools:
        python: "3.10"
      jobs:
        post_checkout:
          # Unshallow the git repository to
          # have access to its full history
          - git fetch --unshallow

In this example, Read the Docs will run ``git clone ...`` as the first command and after that will run ``git fetch --unshallow``.
Then it will continue with the rest of the remaining pre-defined jobs.

To learn more about this how to use this new feature,
read the `build customization <https://docs.readthedocs.io/en/stable/build-customization.html>`_ documentation page.


The future of the builders
--------------------------

We are already discussing how we can expand this feature in the future.
We'd like to support more complex build processes,
or even projects that are not using Sphinx or MkDocs.
That would open the door to a lot new possibilities.
So, subscribe to our mailing list and stay tuned!

Try it out now!
---------------

We encourage you to give it a try now to power up your documentation's build process.
As we mentioned, we are designing the future of our builders and we are collecting ideas from our users.
Your feedback will allow us to ensure our design is flexible and customizable enough,
and that we're supporting as many use cases as possible.

Please, contact us at support@readthedocs.com to let us know how you are using ``build.jobs``!
