.. _pcsx2-guide:

PCSX2
=====

This guide shows you how to set up ReShade with the PCSX2 emulator.

Introduction to PCSX2 Settings
------------------------------

We'll use the DX11 API for this guide because it works well with other add-ons.

Display Settings
^^^^^^^^^^^^^^^^

To find the display settings, go to the menu shown below.

.. figure:: images/pcsx2/PCSX2_Settings00.png

   Screenshot of the PCSX2 display settings menu.

#. **Fullscreen Mode & Aspect Ratio**: Set the aspect ratio to :guilabel:`Fit to Window` as shown below.

   .. figure:: images/pcsx2/PCSX2_Fullscreen_AR.png

      Screenshot showing :guilabel:`Fit to Window` aspect ratio selected.

   This is important because the depth buffer is set this way internally.

#. **Anti-Blur**: Turn on this option to reduce blurry effects.

   .. figure:: images/pcsx2/PCSX2_Anti-Blur.png

      Screenshot showing the :guilabel:`Anti-Blur` option enabled.

Rendering
---------

We'll use the DX11 API for rendering. You can try other APIs if they can output a depth buffer.

Rendering Options
^^^^^^^^^^^^^^^^^

To find the rendering settings, go to the menu shown below.

.. figure:: images/pcsx2/PCSX2_Settings01.png

   Screenshot of the PCSX2 rendering settings menu.

#. **Rendering**: Set the rendering to :guilabel:`Direct3D 11` as shown below.

   .. figure:: images/pcsx2/PCSX2_Renderer.png

      Screenshot showing :guilabel:`Direct3D 11` selected as the renderer.

   This setting works best with most ReShade add-ons.

#. **Internal Resolution**: For most games, set the internal resolution to :guilabel:`Native`.

   .. figure:: images/pcsx2/PCSX2_Rendering.png

      Screenshot showing :guilabel:`Native` resolution selected.

   This also helps ReShade's generic depth add-on work correctly.

Installing and Configuring ReShade
----------------------------------

To use ReShade with PCSX2, follow these steps:

#. **Install ReShade**: Install ReShade using your current API setting. You can find the installation guide `here <../reshade/reshadeversions.md>`_.
#. **Turn off the emulator and install ReShade.**
#. **Start your game and open the ReShade menu.**
#. **Check the depth buffer**: In the add-ons tab, check the depth buffer.

   .. figure:: images/pcsx2/PCSX2_ReShade_Depth_Add-on.png

      Screenshot of the ReShade add-ons tab showing the depth buffer.

Additional Information
----------------------

Make sure you finish any other setup, like configuring games and BIOS, on your own.

Conclusion
----------

This guide gives you a good start for using ReShade with PCSX2. Keep in mind that the best settings might be different for each game.
