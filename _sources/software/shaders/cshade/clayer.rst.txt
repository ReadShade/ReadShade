
cLayer
======

The ``cLayer`` system is a powerful multi-pass framework within CShade designed for advanced image compositing and layering.

What is cLayer?
---------------

``cLayer`` is a framework that allows you to "capture" the state of the image at a specific point in the ReShade technique list and "blend" it back later. It essentially acts as a temporary buffer that can store a snapshot of your visual processing to be used as a source for blending operations in a subsequent pass.

Where to find it?
-----------------

The system is implemented across two main files:

- **Shader**: :file:`cLayer.fx` (Contains the technique and pass definitions).
- **Header**: :file:`cLayer.fxh` (Contains the core logic, macros for creating layers, and instance settings).

When to use it?
---------------

Use ``cLayer`` when you need to:

- **Compare Stages**: Blend a "before" version of an image with an "after" version using a specific blend mode.
- **Complex Compositing**: Create effects that require multiple layers, such as applying a blur to only certain elements and then masking it back.
- **Geometric Adjustments**: Reposition or scale a previous stage of processing independently of the current one.

How to use it?
--------------

Using ``cLayer`` involves a simple three-step process in your ReShade technique list:

1. **Copy Stage**:

   Enable a ``cLayer_CopyLayerN`` shader (e.g., ``CShade | Copy Layer 1``) above the shaders you want to isolate. This captures the current backbuffer into a dedicated texture.

2. **Intermediate Processing**:

   Place any number of shaders below the Copy Layer. These will modify the "current" backbuffer while the Copy Layer texture remains unchanged.

3. **Blend Stage**:

   Enable the corresponding ``cLayer_BlendLayerN`` shader (e.g., ``CShade | Blend Layer 1``) below your intermediate shaders. Use the UI controls to:

   - Select a **Color Blending Mode** (Multiply, Screen, Overlay, etc.).
   - Apply **Geometric Transforms** (Scale, Rotate, Translate) to either the Source or Destination images.
   - Adjust **RGBA Influence** to fine-tune the intensity of the merge.

Why does cLayer exist?
----------------------

ReShade typically executes techniques in a linear, top-to-bottom sequence. This makes it difficult to perform complex compositing tasks that require data from an earlier point in the pipeline. ``cLayer`` overcomes this limitation by providing a structured way to branch and merge the image pipeline, enabling high-level post-processing workflows usually reserved for professional editing software.
