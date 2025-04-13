# Disabling DLSS Frame Generation

## Introduction

This guide provides two methods for disabling DLSS Frame Generation, a feature that can cause crashes when starting or playing games. The first method will disable it globally for all games on Windows, while the second method will demonstrate how to disable it for a specific game.

### Note

You do not need this method on Intel and AMD setups.

## Method 1: Global Disable

To disable DLSS Frame Generation globally, follow these steps:

### Step-by-Step Instructions

1. **Access Display Settings:** Go to `Display Settings` on your Windows system.

    ![](images/dlssfg/dlssfg1.png)

2. **Navigate to Graphics Settings:** Next, go to `System > Display > Graphics` and click on `Change default graphics settings`.

    ![](images/dlssfg/dlssfg2.png)

3. **Locate Hardware Accelerated GPU Scheduling:** After clicking on the above option, look for **`Hardware Accelerated GPU Scheduling`**.

    ![](images/dlssfg/dlssfg3.png)

4. **Disable Hardware Accelerated GPU Scheduling:** Turn off **`Hardware Accelerated GPU Scheduling`**.

    ![](images/dlssfg/dlssfg4.png)

5. **Restart Your PC:** Reset your PC to apply the changes, which should globally disable Frame Generation.

## Method 2: Game-Specific Disable

For this demonstration, we will use **Ghost Runner 2** as an example. Most games will have a similar process.

![](images/dlssfg/dlssfg5.png)

To disable DLSS Frame Generation for a specific game, follow these steps:

### Step-by-Step Instructions

1. **Locate the nvngx_dlssg.dll File:** You will be looking for a file called `nvngx_dlssg.dll`. In this case, it's located in the [Streamline](https://developer.nvidia.com/rtx/streamline) folder:

   ![](images/dlssfg/dlssfg7.png)

2. **Rename the nvngx_dlssg.dll File:** Rename `nvngx_dlssg.dll` to `nvngx_dlssg.back`.

   ![](images/dlssfg/dlssfg8.png)

## Example Screenshot

Here's an example screenshot of the game with DLSS Frame Generation disabled:
![](images/dlssfg/dlssfg6.png)

## Conclusion

![](images/dlssfg/dlssfg9.png)

That's it for now. We will post more examples for other games later. Good luck with disabling DLSS Frame Generation, and we hope this guide has been helpful in resolving any issues you may have encountered.
