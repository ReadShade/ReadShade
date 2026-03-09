
CSHADE_APPLY_GRAIN
==================

A preprocessor macro to enable procedural film grain in the CShade rendering pipeline.

What is CSHADE_APPLY_GRAIN?
---------------------------

``CSHADE_APPLY_GRAIN`` is a macro that adds a dynamic film grain effect to the final image. It uses procedural noise (Simplex noise) to simulate the chemical grain texture found in traditional film stock, adding texture and a sense of "realism" to digital rendering.

Where to find it?
-----------------

- **Logic**: The macro is checked within :file:`shared/cShade.fxh`.
- **Implementation**: The underlying function ``CLens_ApplyFilmGrain`` is located in :file:`shared/cLens.fxh`.

When to use it?
---------------

Use this macro when you want to:

- Break up clean digital gradients and reduce color banding.
- Achieve a classic "filmic" or "vintage" aesthetic.
- Add micro-texture to the image to increase perceived detail.

How to use it?
--------------

Define the macro as ``1`` before including the main CShade header:

.. code-block:: hlsl

   #define CSHADE_APPLY_GRAIN 1
   #include "shared/cShade.fxh"

Once enabled, the UI will provide options to adjust **Grain Size**, **Grain Intensity**, and whether to use a **Time-based Seed** for dynamic movement.

Why does it exist?
------------------

Perfectly smooth digital images can often feel artificial or "sterile." Film grain introduces organic-feeling randomness that mimics the imperfections of physical media. Integrating it directly into the core pipeline ensures it can be applied efficiently as a final texture layer.
