
Implement the Grayscale Logic
=============================

Now, let's modify the ``PS_Grayscale`` function to convert the color to grayscale. A common way to do this is to take the average of the red, green, and blue components, or use a weighted average for a more perceptually accurate grayscale. The ``dot`` product is used here to perform a weighted sum of the color components, which is a standard method for converting RGB to luminance (grayscale).

.. code-block:: hlsl

    #include "ReShade.fxh"

    float3 PS_Grayscale(float4 vpos : SV_Position, float2 texcoord : TexCoord) : SV_Target
    {
        // Read the original color of the pixel
        float3 originalColor = tex2D(ReShade::BackBuffer, texcoord).rgb;

        // Calculate the grayscale value (weighted average for better perception)
        // The dot product multiplies each color component (R, G, B) by a specific weight
        // and sums the results. These weights (0.299, 0.587, 0.114) are commonly used
        // to approximate human perception of brightness.
        float grayscaleValue = dot(originalColor, float3(0.299, 0.587, 0.114));

        // Return a color where R, G, and B are all set to the grayscale value
        return float3(grayscaleValue, grayscaleValue, grayscaleValue);
    }

    technique MyGrayscaleEffect
    {
        pass
        {
            VertexShader = PostProcessVS;
            PixelShader = PS_Grayscale;
        }
    }
