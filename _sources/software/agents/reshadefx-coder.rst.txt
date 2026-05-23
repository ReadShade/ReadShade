
ReShadeFX Coder Skill
=====================

Purpose
-------

The ``reshadefx-coder`` skill provides expert assistance for developing and maintaining ReShadeFX shaders. It is an expert in ReShadeFX (HLSL), capable of finding bugs, generating new shader code, and suggesting optimized revisions while strictly adhering to established conventions.

Core Capabilities
-----------------

- **Bug Investigation**: Identify common ReShadeFX and HLSL errors (syntax errors, resource mismatches, logical flaws).
- **Code Generation**: Create new :file:`.fx` and :file:`.fxh` files, including vertex/pixel shaders, texture declarations, and pass definitions.
- **Optimization**: Suggest and implement performance-oriented revisions (hardware blending, precision management, register usage).
- **Standards & Conventions**: Ensure all new code follows standard ReShadeFX naming and UI conventions.

Usage
-----

This skill is intended to be used with an AI agent (such as Gemini CLI or Claude Code) when working on ReShadeFX shader projects (like `CShade <https://github.com/CeeJayDK/CShade>`_ or any ReShadeFX repository).

Common Workflows
^^^^^^^^^^^^^^^^

Finding Bugs
""""""""""""

When asked to find bugs in a shader, the skill analyzes the :file:`.fx` and any included :file:`.fxh` files, checks for adherence to coding conventions, and identifies common pitfalls like uninitialized variables or out-of-bounds texture access.

Feature Implementation
""""""""""""""""""""""

The skill can draft a plan using ReShade's macro-based DSL and existing implementations in the project for similar logic. All new uniforms and functions follow ReShade-specific standards.

Performance Review
""""""""""""""""""

The skill identifies bottlenecks (e.g., redundant texture lookups or complex branching) and applies optimization principles like hardware-accelerated blending and proper precision management (``float`` vs ``half``).

Example Requests
^^^^^^^^^^^^^^^^

You can ask the AI agent to:

- *"Find any syntax or logical errors in this shader file."*
- *"Implement a new bloom effect based on the provided algorithm."*
- *"Optimize this pixel shader to use hardware blending instead of manual math."*
- *"Add a UI slider to control the intensity of this effect, following the category conventions."*
