
# ReadShade

## Project Overview

ReadShade is a Sphinx documentation project designed to be a neutral and simple platform for sharing knowledge about ReShade, Depth3D, emulators, games, and hardware.

## Technologies Used

This project utilizes:

- **[Sphinx](https://www.sphinx-doc.org/):** For generating documentation.
- **[reStructuredText (.rst)](https://docutils.sourceforge.io/rst.html):** The markup language used for writing documentation.
- **[Furo Theme](https://pradyunsg.me/furo/):** The visual theme applied to the documentation.
- **[Python](https://www.python.org/):** The programming language used for Sphinx.
- **[pip](https://pip.pypa.io/):** Python package installer for managing dependencies.
- **Makefile/make.bat:** For building the documentation on Unix-like systems and Windows, respectively.

## Offline Access / Building Locally

To view the documentation offline or build it locally, follow these steps:

1. **Download ReadShade:** You have two options to get the project files:

    - **Clone the repository (recommended):**

        ```bash
        git clone https://github.com/ReadShade/ReadShade.git
        cd ReadShade
        ```

    - **Download as ZIP/TAR:**

        - Go to the [ReadShade GitHub page](https://github.com/your-username/ReadShade) and click on the green "Code" button.
        - Then, select "Download ZIP" or "Download TAR" and extract the contents to your desired location.
        - Navigate into the extracted directory.

2. **Install Dependencies:** Ensure you have Python and pip installed. Then, install the project dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. **Build Documentation:**

    - **On Unix-like systems (Linux, macOS):**

        ```bash
        make html
        ```
    - **On Windows:**

        ```bash
        make.bat html
        ```

4. **View Documentation:** The generated HTML files will be located in the `build/html` directory. Open `index.html` in your web browser to access the documentation.
