
Understanding Key Concepts
==========================

``float3``, ``float4``
    These are vector types used to store multiple floating-point numbers. For example, ``float3`` is commonly used for RGB color values (red, green, blue) or 3D coordinates (x, y, z). ``float4`` can store RGBA color (red, green, blue, alpha) or 4D vectors.

``tex2D(sampler, texcoord)``
    This is a crucial function for reading data from textures. It takes two main arguments:

    - ``sampler``: Specifies *how* to read the texture (e.g., ``ReShade::BackBuffer`` for the game's original image).
    - ``texcoord``: A ``float2`` value representing the normalized 2D coordinates on the texture, ranging from (0,0) (top-left) to (1,1) (bottom-right).

``SV_Position``, ``TexCoord``, ``SV_Target``
    These are called **semantics**, which are special keywords that tell the graphics card what kind of data a variable represents and how it should be used in the rendering pipeline. They act as a bridge between different shader stages.

    - ``SV_Position``: Used to represent the screen-space position of a vertex (in a vertex shader) or a pixel (in a pixel shader).
    - ``TexCoord``: Represents texture coordinates, indicating which part of a texture to sample.
    - ``SV_Target``: Designates the output color of a pixel shader, which will be written to the render target (e.g., your screen).

``uniform``
    As discussed, the ``uniform`` keyword declares a variable whose value is constant across an entire shader pass but can be set externally. The ``< ui_type = "combo"; ui_items = "..." >`` syntax is an **annotation**. These annotations are specific to ReShade FX and provide instructions to the ReShade UI on how to display and allow the user to interact with that uniform variable (e.g., as a slider, a dropdown combo box, or a checkbox).
