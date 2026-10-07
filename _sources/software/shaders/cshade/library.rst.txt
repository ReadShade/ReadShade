
Library
=======

CShade includes a comprehensive library of shared header files (:file:`.fxh`) that provide the foundation for its shaders. These headers contain various algorithms, mathematical functions, and utility macros used throughout the collection.

Shared Headers
--------------

.. csv-table::
   :header-rows: 1

   Location, Purpose
   :file:`shared/cBlend.fxh`, "Macros, blend states, and functions for managing color and alpha blending operations."
   :file:`shared/cBlur.fxh`, "Collection of blur-related functions and algorithms (Gaussian, Dual Kawase, Box, etc.)."
   :file:`shared/cCamera.fxh`, "Functions and UI controls for auto-exposure and exposure peaking."
   :file:`shared/cColor.fxh`, "Library of color manipulation functions, blend modes, and color space conversions."
   :file:`shared/cComposite.fxh`, "Comprehensive color grading and tonemapping pipeline."
   :file:`shared/cEdge.fxh`, "Edge detection filters (Sobel, Prewitt, Scharr, Frei-Chen)."
   :file:`shared/cLens.fxh`, "Lens-related visual effects (film grain, chromatic aberration, vignetting)."
   :file:`shared/cMacros.fxh`, "General-purpose macros and bitwise operations."
   :file:`shared/cMath.fxh`, "Mathematical functions, geometric transforms, and noise generators."
   :file:`shared/cMotionEstimation.fxh`, "Real-time motion estimation using Lucas-Kanade optical flow."
   :file:`shared/cShade.fxh`, "Core utility library, buffer management, and standard rendering pipeline."
