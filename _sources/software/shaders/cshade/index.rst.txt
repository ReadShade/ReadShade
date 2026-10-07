
CShade
======

CShade is a collection of HLSL shaders for ReShade that introduces conventional image and video processing effects from a different angle. It includes a variety of tools for image enhancement, motion estimation, and post-processing aesthetics.

Features
--------

CShade stands out with several unique features and a highly modular design:

- **Inter-Shader Merging**: Allows users to blend multiple shaders together and configure specific channel outputs (Red, Green, Blue, and Alpha).
- **Adaptive Exposure**: Features an auto-exposure system using hardware blending for smooth temporal transitions and spot-metering for localized brightness adjustment.
- **Comprehensive Processing Suite**:

  - **Image Processing**: Sharpening (CAS, RCAS), Anti-Aliasing (FXAA, DLAA), and various convolutions.
  - **Video Processing**: Real-time motion shaders including Optical Flow (Lucas-Kanade), Datamoshing, and Motion Blur.
  - **Post Processing**: High-quality Bloom, Color Grading, and Lens effects.

UI Markers
----------

CShade shaders use specific markers in the UI to indicate requirements or characteristics:

- **[D] Depth Buffer**: Requires access to the depth buffer to function correctly.
- **[&] Linked**: Requires another shader to be enabled and positioned correctly in the technique list.
- **[+] Preprocessor**: Supports extra features via preprocessor definitions.
- **[!] Caution**: Significant limitations or potential breaking changes.
- **[?] Info**: General notes or usage tips.
- **[$] Expensive**: High performance demand; may impact frame rates.

Shader Reference
----------------

.. csv-table::
   :header-rows: 1

   Filename, "UI Label", "Purpose"
   :file:`cAutoExposure.fx`, "CShade | Auto Exposure", "Standalone lightweight, adjustable auto exposure."
   :file:`cBloom.fx`, "CShade | Bloom", "Adjustable bloom with integrated auto-exposure."
   :file:`cBlurH.fx`, "CShade | Horizontal Blur", "Horizontal Gaussian blur effect."
   :file:`cBlurV.fx`, "CShade | Vertical Blur", "Vertical Gaussian blur effect."
   :file:`cCAS.fx`, "CShade | CAS", "AMD FidelityFX Contrast Adaptive Sharpening."
   :file:`cCheckerBoard.fx`, "CShade | Checkerboard", "Adjustable checkerboard pattern generator."
   :file:`cDLAA.fx`, "CShade | DLAA", "Directionally Localized Anti-Aliasing."
   :file:`cDots.fx`, "CShade | Dots", "Halftone-like dot pattern based on image features."
   :file:`cEnsor.fx`, "CShade | Censor", "Feature-based pixelation for censorship effects."
   :file:`cFXAA.fx`, "CShade | FXAA", "Fast Approximate Anti-Aliasing."
   :file:`cFlow.fx`, "CShade | Optical Flow", "Lucas-Kanade optical flow visualization."
   :file:`cGhost.fx`, "CShade | Ghosting", "Ethereal ghosting effect through frame-blending."
   :file:`cLayer.fx`, "CShade | Layer System", "Multi-pass framework for copying and blending buffers."
   :file:`cLens.fx`, "CShade | Lens", "Lens effects (grain, chromatic aberration, vignette)."
   :file:`cLetterBox.fx`, "CShade | Letterbox", "Cinematic aspect ratio black bars."
   :file:`cLipse.fx`, "CShade | Color Grade", "Standalone, adjustable color grading system."
   :file:`cMotionBlur.fx`, "CShade | Motion Blur", "Flow-based motion blur effect."
   :file:`cMotionStabilization.fx`, "CShade | Stabilization", "Flow-based camera shake stabilization."
   :file:`cNoiseBlur.fx`, "CShade | Noise Blur", "Artistic noise-based blur effect."
   :file:`cNormalize.fx`, "CShade | Normalize", "Local contrast normalization and Census transform."
   :file:`cQuantize.fx`, "CShade | Quantize", "Artificial color quantization and dithering."
   :file:`cRCAS.fx`, "CShade | RCAS", "AMD FidelityFX Robust Contrast Adaptive Sharpening."
   :file:`cSolidColor.fx`, "CShade | Solid Color", "Simple solid color overlay."
   :file:`cSpace.fx`, "CShade | Color Spaces", "Visualization of grayscale and chromaticity spaces."
   :file:`cThreshold.fx`, "CShade | Threshold", "Luminance-based thresholding and extraction."
   :file:`cTransform.fx`, "CShade | Transform", "Geometric and color transformations with overlays."
   :file:`kContour.fx`, "CShade | KinoContour", "Gradient-based contour line filter."
   :file:`kDatamosh.fx`, "CShade | KinoDatamosh", "Video compression artifact simulation."
   :file:`kMirror.fx`, "CShade | KinoMirror", "Symmetrical mirroring and kaleidoscope effects."

Advanced Documentation
----------------------

For more in-depth information on CShade's specialized features and core pipeline configuration, refer to the following guides:

.. toctree::
   :maxdepth: 2

   clayer
   library
   macros/index
