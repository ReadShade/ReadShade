
Welcome to ReadShade
====================

ReadShade is a documentation site designed with simplicity and neutrality in mind. We aim to provide a straightforward and accessible platform for everyone to contribute and share knowledge. We've removed unnecessary complexity and barriers, ensuring that anyone can join our community.

Striving for Neutrality
-----------------------

We strive to remain neutral in our approach, avoiding conflict of interest.

Simple to Contribute
--------------------

We want to make it easy for anyone to contribute to ReadShade, regardless of their technical background. We've chosen Python and Sphinx as our core technologies. You can start creating and editing documentation quickly with just these two tools. There is no need to worry about complicated setup or configuration - install Python and Sphinx, and you're ready to go.

Offline Download
----------------

You can download a complete, static version of this documentation site for offline use. This is useful for accessing guides and information without an internet connection. The instructions below outline two methods for getting the site onto your local machine.


Method 1: Download from the gh-pages branch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This is the most direct method to get the already-built static website without needing to install Python and Sphinx.

#. **Go to the repository:** Navigate to the `ReadShade repository on GitHub <https://github.com/ReadShade/ReadShade>`_.
#. **Switch branches:** Click on the branch dropdown menu \(it usually says :guilabel:`main`\) and select the :guilabel:`gh-pages` branch.
#. **Download the content:** Click on the green :guilabel:`Code` button and select :guilabel:`Download ZIP`.
#. **Extract and view:** Unzip the downloaded file and open the :file:`index.html` file in your web browser. This folder contains the complete, pre-built website.

Method 2: Download the ZIP file
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This is the simplest method for users who do not have Git installed.

#. **Download the repository:** Go to the `ReadShade repository on GitHub <https://github.com/ReadShade/ReadShade>`_.
#. **Click on the "Code" button:** In the top-right corner of the repository page, click the green :guilabel:`Code` button.
#. **Select "Download ZIP":** From the dropdown menu, click on :guilabel:`Download ZIP` to save a compressed file of the repository to your computer.
#. **Extract the files:** Unzip the downloaded file to a location on your local machine.
#. **Build the site:** Open a terminal or command prompt, navigate to the extracted folder, and run the following commands to install the requirements and build the site:

   .. code-block:: console

      pip install -r requirements.txt
      sphinx-build -b html . _build

6. **Access the offline content:** The static site is now located in the `_build` folder. You can view the documentation by opening the :file:`index.html` file in your preferred web browser.

Method 3: Clone the repository
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This method is recommended for users who have Git installed and want to keep their local copy updated.

#. **Clone the repository:** Open your terminal or command prompt and run the following command to clone the documentation site's repository to your local machine.

   .. code-block:: console

      git clone https://github.com/ReadShade/ReadShade.git

#. **Navigate to the directory:** Change your current directory to the cloned repository.

   .. code-block:: console

      cd ReadShade

#. **Install requirements and build the site:** Run the following commands to install the necessary Python packages and build the static HTML site.

   .. code-block:: console

      pip install -r requirements.txt
      sphinx-build -b html . _build

#. **Access the offline content:** The static site is now located in the `_build` folder. You can view the documentation by opening the :file:`index.html` file in your preferred web browser.

Acknowledgements & Contributors
-------------------------------

* `The Depth3D Crew <https://blueskydefender.github.io/Depth3D/>`_
* `[R-DEV]papadanku <https://github.com/papadanku>`_

.. toctree::
   :glob:
   :hidden:

   reshade/index
   */index
