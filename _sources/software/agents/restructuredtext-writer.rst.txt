
reStructuredText Writer Skill
=============================

Purpose
-------

The ``restructuredtext-writer`` skill provides expert guidance for processing reStructuredText (RST) files, building Sphinx documentation, and ensuring high-quality content. It is specifically designed to help maintain documentation projects like ReadShade.

Core Capabilities
-----------------

- **Content Creation**: Expert assistance in writing and updating documentation using plain English and an active voice.
- **Project Setup**: Guidance on creating new Sphinx projects with ``sphinx-quickstart``.
- **Formatting**: Large-scale formatting and linting recommendations (e.g., using ``doc8`` or ``restructuredtext-lint``).
- **Advanced RST**: Detailed explanations and examples for directives, roles, tables, and cross-referencing.
- **Build Management**: Assistance with compiling HTML documentation and managing multiple builders (PDF, EPUB).

Usage
-----

This skill is intended to be used with an AI agent (such as Gemini CLI or Claude Code) when working within a Sphinx-based documentation project.

Compiling Documentation
^^^^^^^^^^^^^^^^^^^^^^^

To build the HTML version of the documentation (like ReadShade):

.. code-block:: bash
   :caption: On Linux/macOS

   make html

.. code-block:: console
   :caption: On Windows

   .\make.bat html

The output will typically be located in the :file:`build/html/` or :file:`_build/html/` directory.

Documentation Assistance
^^^^^^^^^^^^^^^^^^^^^^^^

You can ask the AI agent to:

- *"Add a new section about [topic] to the index page."*
- *"Format this table correctly in reStructuredText."*
- *"Check for broken links or linting errors in this file."*
- *"Explain how to use the ``toctree`` directive with the ``:glob:`` option."*
