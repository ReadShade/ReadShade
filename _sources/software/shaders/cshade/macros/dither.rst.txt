
CSHADE_APPLY_DITHER
===================

A preprocessor macro to enable dithering in the CShade rendering pipeline to minimize banding artifacts.

What is CSHADE_APPLY_DITHER?
----------------------------

``CSHADE_APPLY_DITHER`` is a configuration macro that applies a controlled noise pattern to the final output. This process, known as dithering, is used to randomize quantization errors, effectively masking color banding that occurs when representing high-precision color data in lower bit-depth buffers (like standard 8-bit monitors).

Where to find it?
-----------------

- **Logic**: The macro is checked within :file:`shared/cShade.fxh`.
- **Implementation**: The underlying logic is in :file:`shared/cComposite.fxh` and :file:`shared/cMath.fxh`.

When to use it?
---------------

You should enable dithering when:

- You notice "steps" or "rings" in smooth gradients (e.g., in the sky or shadows).
- You are performing heavy color grading or using effects that increase contrast.
- You want to maintain the illusion of high color depth on standard displays.

How to use it?
--------------

Define the macro as ``1`` before including the main CShade header:

.. code-block:: hlsl

   #define CSHADE_APPLY_DITHER 1
   #include "shared/cShade.fxh"

In the ReShade UI, you can toggle the effect and select between different algorithms like **Golden Ratio Noise**, **Interleaved Gradient Noise**, or **White Noise**.

Why does it exist?
------------------

Digital displays have limited precision. When shaders perform complex math, the resulting colors often fall between the discrete levels a monitor can display. Without dithering, these colors are rounded, leading to visible banding. Dithering uses the human eye's natural tendency to "average" nearby pixels, creating the appearance of smooth transitions where none physically exist.
