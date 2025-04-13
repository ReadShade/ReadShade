# Deleting Post Effects on Unreal Engine

## Introduction

This guide provides instructions on how to delete or disable post effects on Unreal Engine 4 and Unreal Engine 5 games. The steps outlined in this guide can help improve performance and reduce visual issues.

## Unreal Engine 4

The following post effects can be disabled in Unreal Engine 4 games:

* Motion Blur
* Depth of Field
* Chromatic Aberration

### Phase 1: Editing the Engine.ini File

To disable these effects, follow these steps:

1. **Locate the Engine.ini File:** Head over to `%APPDATA%` or `%LOCALAPPDATA%` and navigate to the game's configuration directory:

    * **Steam:** `"GAME"\Saved\Config\WindowsNoEditor`
    * **Windows Game Store:** `"GAME"\Saved\Config\WinGDK`

2. **Edit the Engine.ini File:** Open the `Engine.ini` file and add the following lines at the bottom:

```ini
[SystemSettings]
r.DepthOfFieldQuality=0
r.MotionBlur.Max=0
r.MotionBlurQuality=0
r.DefaultFeature.MotionBlur=0
r.SceneColorFringe.Max=0
r.SceneColorFringeQuality=0
```

3. **Save and Set to Read-Only:** Save the file and set it to `Read Only` to prevent accidental changes.

### Notes

* Keep in mind that changing settings in-game may require a restart to apply the changes made to the `Engine.ini` file.
* This method may not work in every instance, and results may vary.
* For more information on modding the `Engine.ini` file, visit the [PC Gaming Wiki](https://www.pcgamingwiki.com/).

## Unreal Engine 5

Unreal Engine 5 games require different settings to disable post effects. The following example is for HellBlade 2:

```ini
[SystemSettings]
r.SceneColorFringeQuality=0
r.Tonemapper.GrainQuantization=0
r.Tonemapper.Quality=0
r.NT.Lens.Distortion.Intensity=0
r.NT.Lens.Distortion.Stretch=0
r.NT.Lens.ChromaticAberration.Intensity=0
r.NT.DOF.RotationalBokeh=0
r.NT.DOF.NTBokehTransform=0
r.FilmGrain=0
```

To remove letterboxing, add the following lines:

```ini
r.NT.AllowAspectRatioHorizontalExtension=0
r.NT.EnableConstrainAspectRatio=0
```

### Note

Unreal 5 games will be a **case-by-case basis** until we release an addon to disable specific effects.

## Shader Toggler

The Shader Toggler is a free ReShade add-on that can disable certain effects that may cause issues with Depth3D. You can learn more about it in our [ReShade guide](../reshade/reshadeversions.md).

## Upcoming Content

A video guide on deleting post effects on Unreal Engine is coming soon. Stay tuned for more updates and tutorials! 📹
