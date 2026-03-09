Agent Skills
============

:Authors: The ReadShade Team
:Source Code: https://github.com/ReadShade/skills
:Specification: https://agentskills.io/specification

ReadShade provides a collection of specialized AI Agent Skills designed to extend the capabilities of AI development tools. These skills enable AI agents to assist with documentation, shader development, and other specialized tasks within the ReShade ecosystem.

Installation
------------

AI Agent Skills can be installed either globally for all projects or locally within a specific project. Installation involves copying the skill's directory into a location where your AI agent can discover it.

Discovery Paths
^^^^^^^^^^^^^^^

The following table lists the search paths for supported AI agents:

.. list-table::
   :header-rows: 1

   * - AI Agent
     - Global Path
     - Project Path
   * - **Gemini CLI**
     - :file:`~/.gemini/skills/`
     - :file:`./.agents/skills/`
   * - **Claude Code**
     - :file:`~/.claude/skills/`
     - :file:`./.claude/skills/`
   * - **Mistral Vibe**
     - :file:`~/.vibe/skills/`
     - :file:`./.vibe/skills/`

How to Install
^^^^^^^^^^^^^^

1. **Download the Skills**: Clone the `ReadShade skills repository <https://github.com/ReadShade/skills>`_ or download a specific skill folder.
2. **Identify the Target Path**: Choose between global or project-specific installation based on the discovery paths above.
3. **Copy the Skill Folder**: Copy the specific skill's directory (e.g., :file:`reshadefx-coder/`) into your chosen target path.

.. tip::

   For project-specific use, it is recommended to symlink the :file:`skills/` directory to your project's root (e.g., into :file:`./.agents/skills/` for Gemini CLI). This allows you to easily update all skills at once.

Available Skills
----------------

The following skills are currently available:

.. toctree::
   :maxdepth: 1
   :glob:

   *
