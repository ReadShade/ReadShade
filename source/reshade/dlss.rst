
Disabling DLSS Frame Generation
===============================

Introduction
------------

This guide provides two methods for disabling DLSS Frame Generation, a feature that can cause crashes when starting or playing games. The first method will disable it globally for all games on Windows, while the second method will demonstrate how to disable it for a specific game.

.. admonition:: Note

   You do not need this method on Intel and AMD setups.

Method 1: Global Disable
------------------------

To disable DLSS Frame Generation globally, follow these steps:

Step-by-Step Instructions
^^^^^^^^^^^^^^^^^^^^^^^^^

#. **Access Display Settings:** Go to :guilabel:`Display Settings` on your Windows system.

   .. figure:: images/dlssfg/dlssfg1.png

      Display Settings page.

#. **Navigate to Graphics Settings:** Next, go to :menuselection:`System --> Display --> Graphics` and click on :guilabel:`Change default graphics settings`.

   .. figure:: images/dlssfg/dlssfg2.png

      Graphics settings page.

#. **Locate Hardware Accelerated GPU Scheduling:** After clicking on the above option, look for **Hardware Accelerated GPU Scheduling**.

   .. figure:: images/dlssfg/dlssfg3.png

      Hardware Accelerated GPU Scheduling option.

#. **Disable Hardware Accelerated GPU Scheduling:** Turn off **Hardware Accelerated GPU Scheduling**.

   .. figure:: images/dlssfg/dlssfg4.png

      **Hardware Accelerated GPU Scheduling** turned off.

#. **Restart Your PC:** Reset your PC to apply the changes, which should globally disable Frame Generation.

Method 2: Game-Specific Disable
-------------------------------

For this demonstration, we will use **Ghost Runner 2** as an example. Most games will have a similar process.

.. figure:: images/dlssfg/dlssfg5.png

   Ghost Runner 2 game title.

To disable DLSS Frame Generation for a specific game, follow these steps:

Step-by-Step Instructions
^^^^^^^^^^^^^^^^^^^^^^^^^

#. **Locate the nvngx_dlssg.dll File:** You will be looking for a file called :file:`nvngx_dlssg.dll`. In this case, it's located in the `Streamline <https://developer.nvidia.com/rtx/streamline>`_ folder:

   .. figure:: images/dlssfg/dlssfg7.png

      Location of the nvngx_dlssg.dll file.

#. **Rename the nvngx_dlssg.dll File:** Rename :file:`nvngx_dlssg.dll` to :file:`nvngx_dlssg.back`.

   .. figure:: images/dlssfg/dlssfg8.png

      File being renamed.

Example Screenshot
------------------

Here's an example screenshot of the game with DLSS Frame Generation disabled:

.. figure:: images/dlssfg/dlssfg6.png

   Game screenshot with DLSS Frame Generation disabled.

Conclusion
----------

.. figure:: images/dlssfg/dlssfg9.png

   Thank you for reading the guide.

That's it for now. We will post more examples for other games later. Good luck with disabling DLSS Frame Generation, and we hope this guide has been helpful in resolving any issues you may have encountered.
