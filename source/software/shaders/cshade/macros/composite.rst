
CSHADE_COMPOSITE
================

A preprocessor macro to enable the advanced color grading and tonemapping pipeline in CShade.

What is CSHADE_COMPOSITE?
-------------------------

``CSHADE_COMPOSITE`` is a powerful configuration macro that activates the comprehensive color processing suite of CShade. When defined, it enables a high-quality pipeline that includes exposure adjustments, saturation control, log-space contrast, and sophisticated Lift/Gamma/Gain color balancing.

Where to find it?
-----------------

- **Logic**: The macro is checked within :file:`shared/cShade.fxh`.
- **Implementation**: The core grading functions are found in :file:`shared/cComposite.fxh` and :file:`shared/cColor.fxh`.

When to use it?
---------------

This macro is essential when you need:

- **Professional Color Correction**: Precise control over shadows, midtones, and highlights.
- **Tonemapping**: To map high-dynamic-range (HDR) colors to the standard-dynamic-range (SDR) of your monitor.
- **Stylized Looks**: Creating specific visual atmospheres (e.g., filmic, high-contrast, or color-tinted aesthetics).

How to use it?
--------------

Define the macro before including the main CShade header:

.. code-block:: hlsl

   #define CSHADE_COMPOSITE
   #include "shared/cShade.fxh"

Enabling this macro will populate the ReShade UI with numerous controls for **Exposure**, **Contrast**, **Saturation**, and individual color tints for **Shadows**, **Midtones**, and **Highlights**.

Why does it exist?
------------------

Standard image processing often lacks the depth required for high-end visual storytelling. ``CSHADE_COMPOSITE`` exists to provide a standardized, highly optimized, and mathematically accurate color pipeline that ensures consistent and professional-grade results across all CShade shaders.
