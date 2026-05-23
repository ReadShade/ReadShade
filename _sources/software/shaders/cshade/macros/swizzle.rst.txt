
CSHADE_APPLY_SWIZZLE
====================

A preprocessor macro to enable channel remapping and debug output modes in CShade.

What is CSHADE_APPLY_SWIZZLE?
-----------------------------

``CSHADE_APPLY_SWIZZLE`` is a configuration and diagnostic macro that enables "swizzling"—the ability to redirect color and alpha channels. This allows you to remap the Red, Green, Blue, or Alpha output to any other channel from the source, or to isolate specific channels for detailed visual inspection.

Where to find it?
-----------------

- **Logic**: The macro is checked within :file:`shared/cShade.fxh`.
- **Implementation**: The underlying functions ``CComposite_SwizzleChannels`` and ``CComposite_SwapChannels`` are located in :file:`shared/cComposite.fxh`.

When to use it?
---------------

Use this macro when you need to:

- **Debug Shaders**: View only the Alpha channel or a single color component to check for errors or artifacting.
- **Remap Output**: Redirect a specific calculation (e.g., store a mask in the Alpha channel) to a visible color channel for verification.
- **Correct Channel Order**: Quickly swap channels if a particular effect or external tool requires a different RGBA layout.

How to use it?
--------------

Define the macro as ``1`` before including the main CShade header:

.. code-block:: hlsl

   #define CSHADE_APPLY_SWIZZLE 1
   #include "shared/cShade.fxh"

Enabling this macro adds an **Output / Swizzle** category to the UI. You can then use the dropdown menus to map each output channel (e.g., "Map Red Channel To") and use the **DEBUG** menu to isolate a single channel for viewing.

Why does it exist?
------------------

In complex shader development, it's often difficult to see what is happening in a specific channel, especially Alpha. ``CSHADE_APPLY_SWIZZLE`` provides a flexible, built-in toolset for inspecting the raw data of your render targets, significantly simplifying the debugging and optimization process.
