
Add the Basic Structure
=======================

Start by including the :file:`ReShade.fxh` header and defining a basic technique. At this stage, our pixel shader will simply return the original color of the game, serving as a starting point before we introduce any modifications.

.. code-block:: hlsl

   #include "ReShade.fxh"

   // Our pixel shader function will go here
   float3 PS_Grayscale(float4 vpos : SV_Position, float2 texcoord : TexCoord) : SV_Target
   {
      // For now, let's just return the original color
      float3 originalColor = tex2D(ReShade::BackBuffer, texcoord).rgb;
      return originalColor;
   }

   // Our technique
   technique MyGrayscaleEffect
   {
      pass
      {
         VertexShader = PostProcessVS; // Use the standard vertex shader
         PixelShader = PS_Grayscale;   // Use our pixel shader
      }
   }
