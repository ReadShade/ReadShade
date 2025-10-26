
Basic Shader Structure
======================

Every shader in ReShade FX typically consists of a few main parts:

Preprocessor Directives
    These are instructions for the compiler that are processed before the main compilation begins. They are commonly used to include other files (like ``ReShade.fxh``, which provides essential ReShade functions and definitions) or to define constants.

    .. code-block:: hlsl

        #include "ReShade.fxh" // Includes the standard ReShade header

Uniform Variables
    These are variables that remain constant across all pixels or vertices processed in a single shader pass, but their values can be changed from outside the shader, typically through the ReShade in-game user interface (UI). This allows for dynamic adjustments to your effects without recompiling the shader.

    .. code-block:: hlsl

        uniform float Brightness <
            ui_type = "slider"; // Defines this variable as a slider in the ReShade UI
            ui_min = -1.0; ui_max = 1.0; // Sets the minimum and maximum values for the slider
            ui_tooltip = "Adjusts the overall brightness of the scene."; // Tooltip for the UI
        > = 0.0; // Default value for the brightness

Textures and Samplers
    **Textures** are essentially image data or other data grids that the shader can read from. The most frequently used texture is ``BackBufferTex``, which contains the rendered image of your game before any ReShade effects are applied.

    **Samplers** act as the interface for reading from textures. They define *how* a texture is accessed, including aspects like how to handle coordinates that fall outside the texture's boundaries (e.g., ``CLAMP``, ``WRAP``) and the method of filtering (e.g., ``LINEAR`` for smooth blending, ``POINT`` for sharp pixels).

    .. code-block:: hlsl

        // Texture declaration (often found pre-defined in ReShade.fxh)
        texture BackBufferTex : COLOR; // Declares a texture to hold color data

        // Sampler declaration
        sampler BackBuffer
        {
            Texture = BackBufferTex; // Links this sampler to the BackBufferTex
            AddressU = CLAMP; // Clamps texture coordinates to the edge of the texture
            AddressV = CLAMP; // Clamps texture coordinates to the edge of the texture
            MagFilter = LINEAR; // Uses linear interpolation for magnification
            MinFilter = LINEAR; // Uses linear interpolation for minification
        };

Functions (Vertex and Pixel Shaders)
    Vertex Shader (VS)
        This shader stage processes the "vertices" (corner points) of the 3D models in your game world. In the context of ReShade, which primarily deals with post-processing, the vertex shader is often simplified. Its main role is to set up a full-screen rectangle (or "quad") that covers the entire screen, providing the canvas for the pixel shader. You will commonly encounter the standard ``PostProcessVS`` function for this purpose, which is usually provided by ReShade.

        .. code-block:: hlsl

            // Standard Vertex Shader for full-screen effects (often found in ReShade.fxh)
            void PostProcessVS(in uint id : SV_VertexID, out float4 position : SV_Position, out float2 texcoord : TEXCOORD)
            {
                // This code generates vertex positions and texture coordinates for a full-screen quad.
                // SV_VertexID is a system-generated ID for each vertex.
                texcoord.x = (id == 2) ? 2.0 : 0.0;
                texcoord.y = (id == 1) ? 2.0 : 0.0;
                position = float4(texcoord * float2(2.0, -2.0) + float2(-1.0, 1.0), 0.0, 1.0);
            }

    Pixel Shader (PS)
        This is where the core visual effects logic resides. The pixel shader executes for *every single pixel* on your screen (or within the area defined by the vertex shader) and determines its final color. It takes input such as texture coordinates and outputs a color value. Most of your creative work in ReShade FX will happen within pixel shaders.

        .. code-block:: hlsl

            // A simple Pixel Shader that just returns the original color from the back buffer
            float3 PS_Passthrough(float4 vpos : SV_Position, float2 texcoord : TexCoord) : SV_Target
            {
                // tex2D reads a color from the 'BackBuffer' sampler at the given 'texcoord'.
                float3 originalColor = tex2D(BackBuffer, texcoord).rgb;
                return originalColor; // Returns the color for the current pixel
            }

Techniques
    A **technique** acts as a complete rendering pipeline, combining a vertex shader, a pixel shader, and various other rendering settings into a single, executable unit. A single ``.fx`` file can define multiple techniques, each representing a different effect or a variation of an effect.

    .. code-block:: hlsl

        technique MySimpleEffect
        {
            pass // A technique can consist of one or more passes
            {
                VertexShader = PostProcessVS; // Assigns the vertex shader for this pass
                PixelShader = PS_Passthrough; // Assigns our pixel shader for this pass
            }
        }
