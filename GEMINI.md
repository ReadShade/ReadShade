# ReadShade Project Context

## Project Overview
ReadShade is a Sphinx-based documentation project providing a neutral platform for sharing knowledge about ReShade, Depth3D, emulators, and related gaming hardware. It uses the **Shibuya** theme and is written entirely in **reStructuredText (RST)**.

- **Main Technologies:** Python, Sphinx, reStructuredText, Shibuya theme.
- **Project Structure:**
  - `source/`: Contains all documentation source files (`.rst`).
  - `source/reshade/`: ReShade-specific guides (General, Learning, Licensing).
  - `source/software/`: Guides for external software (e.g., PCSX2, ShaderToggler).
  - `source/thirdparty/`: Guides for third-party tools and hardware (e.g., Depth3D, Viture).
  - `source/conf.py`: Sphinx configuration file.
  - `.agents/skills/`: Custom agent skills for specialized tasks.

## Building and Running
To build the documentation locally:

1.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

2.  **Build HTML:**
    - Using Make (Linux/macOS): `make html`
    - Using Batch (Windows): `.\make.bat html`
    - Manual command: `sphinx-build -M html source build`

3.  **View Output:**
    The generated HTML files will be located in `build/html/`. Open `build/html/index.rst` in a browser.

## Development Conventions
- **Markup Language:** Always use reStructuredText (`.rst`). Adhere to standard Sphinx/Docutils directives.
- **Asset Management:** Store images in a local `images/` subdirectory within the same folder as the `.rst` file using them.
- **Navigation:** Root navigation is defined in `source/index.rst`. Domain-specific navigation is handled via `index.rst` files in subdirectories using the `:glob:` option in `toctree`.
- **Tone & Style:** Use plain English and active voice. Content should be neutral and unbiased.
- **AI Integration:** The project explicitly uses Google's Gemini CLI for content creation and revision. Ensure all AI-generated content is reviewed for accuracy and follows the project's neutral tone.

## Specialized Agent Skills
This project includes custom skills to assist with development. Activate them using `activate_skill <name>`:

- **`restructuredtext-writer`**: **(PRIMARY)** Use this for all documentation tasks. It provides expert guidance on RST syntax, Sphinx directives, and building the project.
- **`reshadefx-coder`**: Use this when working on ReShadeFX shader code examples or technical explanations in the `source/reshade/learning/reshadefx/` section.

## Key Files
- `source/conf.py`: Defines the project's metadata, extensions, and theme options.
- `source/index.rst`: The master document and entry point for the documentation.
- `requirements.txt`: List of Python packages required for the project.
- `CONTRIBUTING.md`: Guidelines for external contributors.
