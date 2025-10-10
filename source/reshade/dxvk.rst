DXVK with ReShade
=================

Introduction
------------

This guide will walk you through installing DXVK alongside ReShade. This combination can improve game performance and allow for advanced post-processing effects.

- **DXVK:** Translates DirectX 9, 10, or 11 games to Vulkan, often leading to better performance or compatibility, especially on Linux, but sometimes on Windows too.
- **ReShade:** A post-processing injector that adds advanced graphics filters to games, allowing you to enhance visuals with effects like depth of field, ambient occlusion, and color correction.

Why use them together?
----------------------

You might use DXVK for a performance boost or better compatibility, and then use ReShade on top of that to make your game look even better.

How to Install DXVK with ReShade (Step-by-Step):
------------------------------------------------

Part 1: Install DXVK First
^^^^^^^^^^^^^^^^^^^^^^^^^^

#. **Download DXVK:** Go to the official `DXVK GitHub releases page <https://github.com/doitsujin/dxvk/releases>`_. Look for the latest stable release, which will typically be a :file:`.tar.gz` file (e.g., :file:`dxvk-1.2.3.tar.gz`). Download this file.
#. **Extract DXVK:** Extract the contents of the downloaded :file:`.tar.gz` file using an archiving tool like 7-Zip or WinRAR. After extraction, you'll find a folder containing :file:`x32` and :file:`x64` subfolders. These subfolders contain the necessary :file:`d3d9.dll`, :file:`d3d10.dll`, :file:`d3d11.dll`, and :file:`dxgi.dll` files.
#. **Identify your game's architecture:** Most modern games are 64-bit. If unsure, check the game's installation directory for an :file:`x64` folder or the game's executable properties. Older games might be 32-bit.
#. **Copy DXVK files to your game:**

   * Navigate to your game's main executable folder (where the :file:`.exe` file that launches the game is located).
   * From the extracted DXVK folder, go into either the :file:`x64` or :file:`x32` folder (depending on your game's architecture).
   * Copy the :file:`d3d9.dll`, :file:`d3d10.dll`, :file:`d3d11.dll`, and :file:`dxgi.dll` files from the DXVK folder directly into your game's main executable folder.

.. important::

   You only need the DLLs for the DirectX version your game uses. For example, if your game is DirectX 11, you primarily need :file:`d3d11.dll` and :file:`dxgi.dll`. Copying all of them usually doesn't cause issues.

Part 2: Install ReShade Second
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. **Download ReShade:** Go to the `official ReShade website <https://reshade.me/>`_ and download the latest version of the ReShade installer.
#. **Run the ReShade Installer:**

   - Open the downloaded ReShade installer.
   - Click "Click here to select a game and manage its ReShade installation."
   - Browse to your game's main executable file (the same :file:`.exe` you copied DXVK files to). Select it.
   - ReShade will then ask you to select a rendering API. **This is crucial:** Since you installed DXVK, your game is now effectively running on Vulkan. So, select **"Vulkan"** from the list.
   - ReShade will then ask you which effect packages you want to install. You can select all of them, or just the ones you think you'll use. Click "OK" or "Continue."
   - The installer will download and install the necessary ReShade files.

Part 3: Verify and Configure
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. **Launch the Game:** Start your game as you normally would.
#. **Check for ReShade:** You should see a small gray text overlay at the top of your screen during game startup, indicating that ReShade is loading.
#. **Open ReShade Menu:** Once in the game, press the :kbd:`Home` key (or :kbd:`Pos1` on some keyboards) to open the ReShade overlay.
#. **Configure ReShade:** Follow the on-screen tutorial in ReShade to select and enable effects. You can create your own presets or download existing ones.

Troubleshooting Tips
--------------------

- **Order Matters:** Always install DXVK *before* ReShade.
- **API Selection:** Make sure you select "Vulkan" in the ReShade installer if you're using DXVK.
- **DLL Conflicts:** If you encounter issues, it's often due to conflicting :file:`.dll` files. Ensure only one :file:`dxgi.dll` (or :file:`d3d9.dll` / :file:`d3d11.dll`) is present that is either from DXVK or ReShade, and that ReShade is configured to hook into the correct API (Vulkan). ReShade's Vulkan installation usually handles this by renaming its own DLL to :file:`dxgi.dll` or :file:`d3d11.dll` and then hooking into the DXVK-provided DLL.
- **Game Updates:** Game updates can sometimes overwrite or remove these custom DLLs, so you might need to reinstall them after an update.
