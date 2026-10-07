
CSHADE_APPLY_VIGNETTE
=====================

A preprocessor macro to toggle the vignette effect in the CShade rendering pipeline.

What is CSHADE_APPLY_VIGNETTE?
------------------------------

``CSHADE_APPLY_VIGNETTE`` is a configuration macro that, when enabled, applies a vignette effect—a subtle darkening of the image corners—during the final rendering stage. This helps draw the viewer's eye toward the center of the frame and adds a cinematic quality to the output.

Where to find it?
-----------------

- **Logic**: The macro is checked within :file:`shared/cShade.fxh`.
- **Implementation**: The underlying function ``CLens_ApplyVignette`` is located in :file:`shared/cLens.fxh`.

When to use it?
---------------

Use this macro when you want to:

- Simulate the natural light falloff of real-world camera lenses.
- Enhance the focus on central subjects in your scene.
- Add a stylized, moody, or "framed" look to your post-processing.

How to use it?
--------------

To enable the vignette, define the macro as ``1`` before including the main CShade header in your shader file:

.. code-block:: hlsl

   #define CSHADE_APPLY_VIGNETTE 1
   #include "shared/cShade.fxh"

Once enabled, you can typically adjust the intensity via the ``Vignette Intensity`` slider in the ReShade UI.

Why does it exist?
------------------

Vignetting is a fundamental aesthetic tool in both photography and cinematography. By integrating it directly into the ``CShade_Render`` function, CShade allows the effect to be applied efficiently without the need for an additional shader pass, maintaining high performance while offering essential artistic control.
