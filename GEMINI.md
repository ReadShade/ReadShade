# Project Overview

ReadShade is a Sphinx documentation project aimed at providing a neutral and simple platform for sharing knowledge about ReShade, Depth3D, emulators, games, and hardware. It emphasizes ease of contribution and accessibility of information.

## Technologies Used

*   **Sphinx:** Documentation generator.
*   **reStructuredText (.rst):** Markup language for writing documentation.
*   **Shibuya Theme:** The visual theme applied to the documentation.
*   **Python:** The programming language used for Sphinx.
*   **pip:** Python package installer for managing dependencies.

## Building and Running

To build and run the documentation locally:

1.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
2.  **Build HTML Documentation:**
    ```bash
    sphinx-build -b html . _build
    ```
    Alternatively, you can use the `Makefile`:
    ```bash
    make html
    ```
    The generated static site will be located in the `_build` directory. Open `_build/index.html` in your web browser to view it.

## Development Conventions

*   **Documentation Format:** All documentation is written in reStructuredText (`.rst`) files.
*   **Build System:** Sphinx is used to generate the documentation from the `.rst` source files.
*   **Content Creation:** The ReadShade team utilizes AI, specifically Google's Gemini CLI, to assist in the creation and revision of textual content.
*   **Contribution:** The project aims for simple contributions, requiring only Python and Sphinx installed to start writing and editing documents.
