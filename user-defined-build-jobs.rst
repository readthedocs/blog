.. post:: Apr 4, 2022
   :tags: build, customization, shell
   :author: Manuel
   :location: BCN

.. meta::
   :description lang=en:
      We released user-defined build jobs (``build.jobs`` config key)
      and we'd love it to help you with your custom build process!


Announcing user-defined build jobs
==================================

We are happy to announce a new feature we released in the past weeks to specify user-defined build jobs on Read the Docs.
With this addition, if your project requires custom commands to be run in the middle of the build process,
they can now be executed with the new config key ``build.jobs``.
This opens up a complete world full of new and exciting possibilities to our users.


Background about the build process
----------------------------------

If your project has ever required a custom command to run during the build process,
you had already dealt with the Read the Docs' limitation that doesn't allow you to execute them.
You may ended up writing a hacky solution inside your Sphinx's ``conf.py`` file to workaround this situation and keep building your docs on Read the Docs.

However, besides that solution not being super elegant and not officially supported by Read the Docs,
it has another important limitation: it was only possible to execute all the commands at once *from inside* the Sphinx's build command.
This mean, there was impossible to run a command after clonning the repository, or before starting the Sphinx build process, for example.
Now, with the addition of the new config key ``build.jobs``, all these limitations are gone!


Using ``build.jobs`` config key
-------------------------------

`Read the Docs' build process <https://docs.readthedocs.io/en/stable/builds.html>`_ is pretty well-defined and divided into pre-defined jobs:
``checkout``, ``system_dependencies``, ``create_environment``, ``install``, ``build`` and ``upload``.
Now, with the introduction of ``build.jobs`` config key users can hook these and run pre- and post- jobs with custom commands.

Let's say your project requires to run a command immediately *after* clonning the repository in the ``checkout`` job.
In that case, you will want to use the ``build.jobs.post_checkout`` config key as show in the following example:

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
Finally, it will continue with the rest of the remaining pre-defined jobs.

To know more about all its potential,
read the `build customization <https://docs.readthedocs.io/en/stable/build-customization.html>`_ documentation page.


The future of the builders
--------------------------

We are already discussing how we can expand this feature in the future to support more projects with more complex build processes,
or even projects that are not using Sphinx or MkDocs.
That would open the door to a lot new possibilities. So, subscribe to our newsletter and stay tuned!


Try it out now!
---------------

We encourage you to give it a try now to power up your documentation's build process.
As we mentioned, we are designing the future of our builders and we are collecting ideas from our users.
They will make us to be sure that our design is flexible and customizable enough,
that supports as much use cases as possible without compromising the UX.
Please, contact us at support@readthedocs.com to let us know how you are using ``build.jobs``!
