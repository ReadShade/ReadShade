
Simulated Reality Displays
==========================

Simulated Reality (SR) Displays, formerly known as Dimenco, are now backed by Leia Inc. This guide will help you get SuperDepth3D working on hardware with SR technology.

.. rubric:: Main Website

`<https://www.leiainc.com/>`_

.. rubric:: Hardware Developers Links

* Acer `Spatiallabs <https://www.acer.com/us-en/spatiallabs>`_
* ASUS `Spatial Vision <https://www.asus.com/content/asus-spatial-vision-technology/>`_
* Sony `Spatial Reality <https://pro.sony/ue_US/products/spatial-reality-displays/3d-professional-images>`_

.. admonition:: Please note that this guide is intended for hardware with the SR badge.

   .. figure:: images/sr1.jpg

      SR badge logo

Getting Started with SuperDepth3D
---------------------------------

To use SuperDepth3D with SR Displays, you can follow either the easy text guide or the manual guide.

For a video tutorial, please refer to this `video guide <https://youtu.be/ovXh54DkKbU>`_.

.. figure:: images/sr2.png

   Screenshot of a video guide.
   SuperDepth3D for Simulated Reality Displays.

Easy Text Guide
---------------

To install ReShade and SuperDepth3D, follow these steps:

#. **Download ReShade:** Download the add-on version of `ReShade <https://reshade.me/#download>`_.

   .. figure:: images/sr3.png

      ReShade download page screenshot.

#. **Install ReShade:** Install ReShade by running the ReShade.exe.

   .. figure:: images/sr4.png

      ReShade installer screenshot.

#. **Select Game Executable:** Select or browse for the game's executable. In this example, we will install it in Forza Horizon 4.

   .. figure:: images/sr5.png

      ReShade installer game selection screenshot.

#. **Click Open:** Click the :guilabel:`Open` button.

#. **Select API:** Select the API and click :guilabel:`Next`.

   .. figure:: images/sr6.png

      ReShade installer API selection screenshot.

#. **Select SuperDepth3D:** Select the Depth3D Repo and check :file:`SuperDepth3D.fx`.

   .. figure:: images/sr7.png

      ReShade installer shader selection screenshot.

#. **Click Next:** Click the :guilabel:`Next` button.

#. **Select 3DGameBridgeProjects Add-on:** Make sure to select the :guilabel:`3DGameBridgeProjects` add-on.

   .. figure:: images/sr9.png

      ReShade installer add-on selection screenshot.

   Click :guilabel:`Next` and then :guilabel:`Finish`.

Manual Guide
------------

If you prefer a more manual approach, follow these steps:

#. **Install ReShade:** Install ReShade or inject it into your game, ensuring you use the `add-on version of ReShade <https://reshade.me/#download>`_.

   .. figure:: images/sr10.png

      ReShade installer screenshot.

   If ReShade is already installed, you can skip this step.

#. **Download 3DGameBridge:** Download the latest version of `3DGameBridge <https://github.com/JoeyAnthony/3DGameBridgeProjects/releases>`_.

   .. figure:: images/sr11.png

      3DGameBridge GitHub page screenshot.

#. **Copy Add-ons:** Copy both add-ons or just the one you need, based on the game's architecture.

   .. figure:: images/sr12.png

      Screenshot of the add-on files.

#. **Paste Add-ons:** Paste the add-ons where the game's executable is located or where the ReShade `.dll` is installed.

   .. figure:: images/sr13.png

      Screenshot of the game folder with the add-ons.

   Please start the game to see if it works.

Important Notes
---------------

When starting the game, you may need to set your primary monitor to the Simulated Reality Display. If not, the game may not select the correct screen, resulting in a black screen.

.. figure:: images/sr14.png

   Screenshot of monitor settings.

Additionally, ensure the game is running at its native resolution for the 3D display. If the resolution is too small, the image may appear distorted.

.. figure:: images/sr15.png

   Screenshot of game resolution settings.