
Disable Unreal Engine's Post Effects
====================================

Introduction
------------

This guide explains how to remove or turn off post effects in games made with Unreal Engine 4 and 5. Doing this can make your games run better and look cleaner.

Unreal Engine 4
---------------

You can turn off these post effects in Unreal Engine 4 games:

- Motion Blur
- Depth of Field
- Chromatic Aberration

Phase 1: Editing the Engine.ini File
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To turn off these effects, follow these steps:

#. **Locate the Engine.ini File:** Go to :file:`%APPDATA%` or :file:`%LOCALAPPDATA%` and find your game's configuration folder:

   - **Steam:** :file:`"GAME"/Saved/Config/WindowsNoEditor`
   - **Windows Game Store:** :file:`"GAME"/Saved/Config/WinGDK`

#. **Edit the Engine.ini File:** Open the :file:`Engine.ini` file and add these lines at the very end:

   .. code-block:: ini

      [SystemSettings]
      r.DepthOfFieldQuality=0
      r.MotionBlur.Max=0
      r.MotionBlurQuality=0
      r.DefaultFeature.MotionBlur=0
      r.SceneColorFringe.Max=0
      r.SceneColorFringeQuality=0

#. **Save and Set to Read-Only:** Save the file, then set it to `Read Only` so it can't be changed by accident.

.. admonition:: Notes
   :class: note

   - Remember that changing settings in-game might need a restart to apply the changes you made to the :file:`Engine.ini` file.
   - This method might not always work, and results can be different.
   - For more details on changing the :file:`Engine.ini` file, visit the `PC Gaming Wiki <https://www.pcgamingwiki.com/>`_.

Unreal Engine 5
---------------

Unreal Engine 5 games need different settings to turn off post effects. Here's an example for HellBlade 2:

.. code-block:: ini

   [SystemSettings]
   r.SceneColorFringeQuality=0
   r.Tonemapper.GrainQuantization=0
   r.Tonemapper.Quality=0
   r.NT.Lens.Distortion.Intensity=0
   r.NT.Lens.Distortion.Stretch=0
   r.NT.Lens.ChromaticAberration.Intensity=0
   r.NT.DOF.RotationalBokeh=0
   r.NT.DOF.NTBokehTransform=0
   r.FilmGrain=0

To get rid of letterboxing, add these lines:

.. code-block:: ini

   r.NT.AllowAspectRatioHorizontalExtension=0
   r.NT.EnableConstrainAspectRatio=0

.. note::

   For Unreal 5 games, you'll need to figure out the settings **case-by-case** until we release an add-on to turn off specific effects.

Shader Toggler
--------------

The Shader Toggler is a free ReShade add-on that can turn off certain effects that might cause problems with Depth3D. You can find out more about it in our `ReShade guide <../reshade/reshadeversions>`_.

Upcoming Content
----------------

A video guide on how to remove post effects in Unreal Engine is coming soon. Keep an eye out for more updates and tutorials! 📹
