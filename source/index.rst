
Welcome to ReadShade
====================

ReadShade is a simple and unbiased documentation site. Our goal is to create an easy-to-use platform where everyone can share and learn. We've removed complex steps and obstacles so anyone can join our community.

Striving for Neutrality
-----------------------

We aim to be fair and unbiased in our approach, avoiding any conflicts of interest.

Simple to Contribute
--------------------

We want to make it easy for anyone to add to ReadShade, no matter their technical skills. We use Python and Sphinx as our main tools. You can quickly start writing and editing documents with just these two. There's no need for complicated setup—just install Python and Sphinx, and you're ready.

Offline Download
----------------

You can download a full, static version of this documentation site to use offline. This is helpful for looking at guides and information when you don't have internet. The instructions below show three ways to get the site onto your computer.


Method 1: Download from the gh-pages branch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This is the easiest way to get the ready-made static website without needing to install Python and Sphinx.

#. **Go to the repository:** Visit the `ReadShade repository on GitHub <https://github.com/ReadShade/ReadShade>`_.
#. **Switch branches:** Click the branch dropdown menu (it usually says :guilabel:`main`) and choose the :guilabel:`gh-pages` branch.
#. **Download the content:** Click the green :guilabel:`Code` button and select :guilabel:`Download ZIP`.
#. **Extract and view:** Unzip the downloaded file and open the :file:`index.html` file in your web browser. This folder contains the complete, pre-built website.

Method 2: Download the ZIP file
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This is the simplest method for users who don't have Git installed.

#. **Download the repository:** Go to the `ReadShade repository on GitHub <https://github.com/ReadShade/ReadShade>`_.
#. **Click on the "Code" button:** In the top-right corner of the repository page, click the green :guilabel:`Code` button.
#. **Select "Download ZIP":** From the dropdown menu, click :guilabel:`Download ZIP` to save a compressed file of the repository to your computer.
#. **Extract the files:** Unzip the downloaded file to a location on your computer.
#. **Build the site:** Open a terminal or command prompt, go to the extracted folder, and run these commands to install what's needed and build the site:

   .. code-block:: console

      pip install -r requirements.txt
      sphinx-build -b html . _build

6. **Access the offline content:** The static site is now in the `_build` folder. You can see the documentation by opening the :file:`index.html` file in your web browser.

Method 3: Clone the repository
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This method is best for users who have Git installed and want to keep their local copy updated.

#. **Clone the repository:** Open your terminal or command prompt and run this command to copy the documentation site's repository to your computer.

   .. code-block:: console

      git clone https://github.com/ReadShade/ReadShade.git

#. **Navigate to the directory:** Change your current directory to the folder you just cloned.

   .. code-block:: console

      cd ReadShade

#. **Install requirements and build the site:** Run these commands to install the necessary Python packages and build the static HTML site.

   .. code-block:: console

      pip install -r requirements.txt
      sphinx-build -b html . _build

#. **Access the offline content:** The static site is now in the `_build` folder. You can see the documentation by opening the :file:`index.html` file in your web browser.

Acknowledgements & Contributors
-------------------------------

* `The Depth3D Crew <https://blueskydefender.github.io/Depth3D/>`_
* `[R-DEV]papadanku <https://github.com/papadanku>`_

.. toctree::
   :glob:
   :hidden:

   reshade/index
   */index
