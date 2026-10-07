
Introduction to Shaders and ReShade FX
======================================

Welcome to this guide on writing shaders for ReShade! If you're new to computer graphics or programming, don't worry, this guide is designed to walk you through the basics in plain English.

What is a Shader?
-----------------

Imagine a painter working on a canvas. In computer graphics, the "canvas" is your screen, and the "painter" is a program called a **shader**. Shaders are small programs that run on your graphics card (GPU) and tell each individual pixel on your screen what color it should be, or how it should be lit. They are incredibly fast because they work on many pixels at once!

ReShade and ReShade FX
----------------------

`ReShade <https://reshade.me/>`_ is a generic post-processing injector for games and video software. It allows you to apply a wide variety of visual filters and effects to your games, from subtle color corrections to advanced depth-based effects.

**ReShade FX** is the shading language used by ReShade. It's similar to `HLSL (High-Level Shading Language) <https://docs.microsoft.com/windows/win32/direct3dhlsl/dx-graphics-hlsl>`_, which is used in DirectX. You'll be writing code in ReShade FX to create your own visual effects.
