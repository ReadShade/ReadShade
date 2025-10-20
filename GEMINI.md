# Project Overview

model: gemini-2.5-flash

This is a Sphinx documentation project for "ReadShade". The documentation is written in reStructuredText (`.rst`) and the visual theme is `furo`.

The project aims to be a neutral and simple platform for sharing knowledge about ReShade, Depth3D, emulators, games, and hardware.

# Key Sections

*   **ReShade General:** Information about ReShade, including different versions.
*   **Addons:** Guides and information about ReShade addons.
*   **Depth3D:** Guides and information related to Depth3D.
*   **Emulation Guides:** Guides for using emulators.
*   **Games:** Information about specific games.
*   **Hardware:** Information about hardware related to the topics above.
*   **Licensing:** Information about the project's licensing.

# Building and Running

To build the HTML documentation, you need to have Python and Sphinx installed. You can install the dependencies with pip:

```bash
pip install -r requirements.txt
```

Then, you can build the documentation using the provided `Makefile` (for Unix-like systems) or `make.bat` (for Windows).

**On Unix-like systems:**

```bash
make html
```

**On Windows:**

```bash
make.bat html
```

The generated HTML files will be in the `build/html` directory. You can open the `index.html` file in that directory to view the documentation.

# Development Conventions

*   All documentation is located in the `source` directory.
*   The main entry point for the documentation is `source/index.rst`.
*   Configuration for the Sphinx project is in `source/conf.py`.
*   The documentation is structured into subdirectories for each topic (e.g., `reshade`, `depth3d`, etc.).
*   Each subdirectory has its own `index.rst` file that serves as the entry point for that section.
*   Images and other static files are stored in subdirectories within each section's directory.
