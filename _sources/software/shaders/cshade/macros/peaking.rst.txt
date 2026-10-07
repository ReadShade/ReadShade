
CSHADE_DEBUG_PEAKING
====================

A preprocessor macro to enable exposure peaking for visualizing over-exposed areas.

What is CSHADE_DEBUG_PEAKING?
-----------------------------

``CSHADE_DEBUG_PEAKING`` is a diagnostic configuration macro. When enabled, it provides an overlay that highlights pixels exceeding a certain luminance threshold. It typically uses a high-contrast checkerboard or dithered pattern to make "clipped" or "blown out" areas immediately obvious to the developer or user.

Where to find it?
-----------------

- **Logic**: The macro is checked within :file:`shared/cShade.fxh`.
- **Implementation**: The underlying function ``CComposite_ApplyExposurePeaking`` is located in :file:`shared/cComposite.fxh`.

When to use it?
---------------

Use this macro during the shader development or preset creation process to:

- Identify areas of the image that are losing detail due to extreme brightness.
- Fine-tune auto-exposure or manual exposure settings.
- Ensure that your color grading is not causing unwanted clipping in the highlights.

How to use it?
--------------

Define the macro as ``1`` before including the main CShade header:

.. code-block:: hlsl

   #define CSHADE_DEBUG_PEAKING 1
   #include "shared/cShade.fxh"

In the UI, you will see a **TOOLS - EXPOSURE PEAKING** section where you can toggle the overlay, adjust the **Luminance Threshold**, and change the **Cell Size** of the pattern.

Why does it exist?
------------------

Proper exposure is critical for maintaining image quality. However, it can be difficult to judge clipping by eye, especially on different monitors. Exposure peaking provides an objective, mathematical visualization of the scene's brightness, acting as a professional "zebra" or "peaking" tool found in high-end cameras.
