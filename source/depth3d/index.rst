
Depth3D
=======

Depth3D is a comprehensive suite of post-process shaders and tools designed for ReShade, primarily focused on bringing depth map-based 3D effects to video games. Developed by BlueSkyDefender, it aims to enhance the visual experience by enabling stereoscopic 3D rendering and offering extensive control over these effects.

At its core, Depth3D features **SuperDepth3D**, a powerful shader that generates depth map-based 3D, akin to NVIDIA's Compatibility Mode 3D. This allows users to experience games in a more immersive, three-dimensional way. To simplify the setup process, :file:`Overwatch.fxh` acts as a companion tool, automatically configuring depth and 3D settings for a wide range of games.

Beyond the core 3D rendering, Depth3D includes several other components:

- **Generic Depth add-on:** This component specifically improves depth effects within games, requiring the add-on version of ReShade for functionality.
- **Reshade Effect Shader Toggler (R.E.S.T):** A versatile tool that grants users granular control over game effects. It allows for the isolation of specific parts of a game's rendering (like the UI) and the application of ReShade shaders, including 3D shaders like SuperDepth3D, to chosen elements.

Depth3D also provides extensive support and guides for various hardware, ensuring a broad compatibility:

- **Simulated Reality (SR) Displays:** Detailed instructions are available for integrating SuperDepth3D with SR technology hardware from manufacturers like Acer (Spatiallabs), ASUS (Spatial Vision), and Sony (Spatial Reality).
- **VITURE AR Glasses:** Users of VITURE Gen 1 AR Glasses can find guides for setting up VITURE AR Glasses with SuperDepth3D, with specific instructions tailored for both Intel and NVIDIA GPUs.

Installation typically involves downloading the add-on version of ReShade, installing it alongside the game, selecting the appropriate API, and then choosing SuperDepth3D and the 3DGameBridgeProjects add-on. Manual installation options are also provided for more experienced users. Configuration within ReShade involves setting up the add-on, adjusting specific shader settings like ``REST_UI_MODE`` for R.E.S.T, and fine-tuning elements such as UI isolation and cursor adjustments.

For game compatibility, users are directed to the PCGamingWiki, which maintains a list of ReShade's depth map compatibility.

.. toctree::
   :glob:

   */index
