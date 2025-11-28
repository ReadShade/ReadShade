.. _rest-guide:

Reshade Effect Shader Toggler (R.E.S.T)
=======================================

The Reshade Effect Shader Toggler (R.E.S.T) is a powerful tool that lets you separate game effects and apply ReShade shaders to specific parts of the game.

.. figure:: images/rest/rest.png

   Screenshot of the Reshade Effect Shader Toggler add-on.

Introduction
------------

To begin using R.E.S.T, you need to download the add-on from its `official GitHub page <https://github.com/4lex4nder/ReshadeEffectShaderToggler/releases/tag/v1.3.15>`_.

Downloading and Installing the Add-on
-------------------------------------

The release folder contains several files, like shaders, FX files, a license, and a README. You can ignore the license and README files for now. You'll need to use one of the :file:`.addon#` files; you can drag both into the same folder where your :file:`ReShade.dll` is. This guide will focus on the 64-bit add-on.

Installing the Add-on
---------------------

Put the :file:`ReshadeEffectShaderToggler.addon64` file in the same place where you installed ReShade. This is usually in your game's folder, next to the :file:`dxgi.dll` file.

Choosing a Game
---------------

For this guide, we will use the game `Wiz⊙rdum <https://store.steampowered.com/app/1715590/Wizordum/>`_. However, you can use R.E.S.T with other games as well.

Setting Up the Add-on
---------------------

Your game folder should look like this:

.. figure:: images/rest/wizordum.png

   Screenshot of the game folder with the add-on installed.

Make sure ReShade is installed and the add-on file is in the correct spot.

Launching the Game and Add-on
-----------------------------

Start the game. ReShade should load with the add-on active. You can find the add-on in the :guilabel:`Add-on` Tab:

.. figure:: images/rest/rest1.png

   Screenshot of the ReShade add-on tab.

Click the arrow to open the add-on, and close other add-ons to make it easier to see.

Configuring the Add-on
----------------------

The add-on menu should look like this:

.. figure:: images/rest/rest2.png

   Screenshot of the opened add-on configuration menu.

Close the ReShade menu and go back into the game to use the add-on.

Setting Up the Add-on in-game
-----------------------------

Open ReShade, move it to the right, and click :guilabel:`New`.

.. figure:: images/rest/rest3.png

   Screenshot showing the :guilabel:`New` button in the ReShade menu.

.. figure:: images/rest/rest4.png

   Screenshot of the new window that appears.

.. rubric:: A new window will open

.. figure:: images/rest/rest5.png

   Screenshot of the add-on configuration window.

.. rubric:: Follow These Steps

1. Click :guilabel:`Activate [x]` (to turn it on)
2. Click :guilabel:`Edit`
3. Type a name in the :guilabel:`Name` field
4. Create a :guilabel:`Shortcut` (a key combination to quickly use it)
5. Click :guilabel:`OK`

Enabling 3D Shader
------------------

If you want to use SuperDepth3D with R.E.S.T, you need to turn on the 3D shader. Open the main menu, enable the 3D shader, and scroll to the very bottom of the shader settings. Set ``REST_UI_MODE`` to ``1`` to enable it:

.. figure:: images/rest/rest8.png

   Screenshot of the shader settings showing REST_UI_MODE.

Configuring the Add-on Settings
-------------------------------

Go back to the Add-on Tab and click :guilabel:`Settings`:

.. figure:: images/rest/rest7.png

   Screenshot of the "Settings" button.

.. rubric:: A new window will open

.. figure:: images/rest/rest9.png

   Screenshot of the add-on settings window.

.. rubric:: Follow These Steps

1. Uncheck :guilabel:`Apply all enabled techniques [ ]`
2. Check the 3D shader :guilabel:`[x]`

.. figure:: images/rest/rest11.png

   Screenshot of the settings after marking the 3D shader.

Isolating the UI
----------------

Look at the list of active buffers:

.. figure:: images/rest/rest12.png

   Screenshot of the active buffers list.

Find the buffer that controls the UI. Double-click its hex value to select it:

.. figure:: images/rest/rest14.png

   Screenshot of a selected hex value.

The selected buffer should turn yellow.

Saving Your Progress
--------------------

Close the window and click :guilabel:`Save all Toggle Groups` to save your changes:

.. figure:: images/rest/rest15.png

   Screenshot of the "Save all Toggle Groups" button.

Troubleshooting
---------------

You might see problems with the center crosshair. Here are three ways to fix this:

1. See if the game lets you remove it.
2. Use the :doc:`ShaderToggler <shadertoggler>`.
3. Change the game files (mod) to remove the texture.

Cursor Adjustments
------------------

If your cursor has issues in Side by Side and Top n Bottom modes, go to :guilabel:`Shader Settings` and find :guilabel:`Cursor Adjustments`:

.. figure:: images/rest/rest18.png

   Screenshot of the "Cursor Adjustments" menu.

Choose your preferred cursor type:

.. figure:: images/rest/rest19.png

   Screenshot of the cursor type options.

You can press :kbd:`Mouse 5` to switch between layers.

Sharing Your Configuration
--------------------------

When you click :guilabel:`Save all Toggle Groups`, a file named :file:`ReshadeEffectShaderToggler.ini` is created in the same folder as the add-on. You can share this file with others by posting it on the `ReShade forum <https://discord.com/channels/305472403977404416/1248039510244065410>`_.
