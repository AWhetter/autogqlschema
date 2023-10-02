:mod:`autogqlschema`
====================

This extension provides a Sphinx directive for generating documentation for GraphQL schemas.

In order to use this extension,
add :mod:`autogqlschema` to the :confval:`sphinx:extensions`
list in your :doc:`conf.py <sphinx:usage/configuration>` file.

.. code-block:: python

   extensions = ["autogqlschema"]


Directives
----------

.. rst:directive:: .. autogqlschema:: name

   Generates API documentation for a GraphQL schema that's declared in the given set of files.

   The ``name`` argument is an arbitrary identifier given to the schema
   for use by Sphinx in cross-references and URLs to this schema.
   This can be useful for documenting multiple schemas in the same documentation,
   but isn't necessary when documenting a single schema.
   Defaults to ``__gqlschema__``.

   .. rubric:: Options

   .. rst:directive:option:: debug

      When given, the generated API documentation will be written to
      a reStructuredText file in Sphinx's output directory.
      The file will have the same name as the schema, with an ``.rst`` extension.

   .. rst:directive:option:: root-dir

      Default: The directory that contains Sphinx's ``conf.py`` file.

      Defines the location that the ``source-files`` are relative to.
      This can be an absolute or relative path.
      A relative path will be taken relative to the directory that contains Sphinx's ``conf.py`` file.

   .. rst:directive:option:: source-files

      This required option should contain a comma separated list of file names
      and/or glob patterns for the files that contain the GraphQL schema to be documented.
      Relative paths are taken relative to ``root-dir``.

   For example:

   .. code-block:: rst

      .. autogqlschema::
         :root-dir: ../src/mypackage/schema
         :source-files: *.graphql
