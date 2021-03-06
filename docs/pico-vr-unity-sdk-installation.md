# Pico VR Unity SDK Installation

## Download the Pico VR Unity SDK

To download the latest unitypackage from WEARVR, you will need a [developer account](https://users.wearvr.com/developers/devices).

You can then [download the Pico VR Unity SDK](https://api.wearvr.com/api/v3/developers/devices/pico-goblin/resources/vr-unity-package).

## Importing the unitypackage

The Pico Unity VR SDK comes as a .unitypackage that you can import into your project via the **Assets › Import Package › Custom Package...** menu option in Unity.

<p align="center">
  <img alt="Import the .unitypackage as custom package"  width="500px" src="assets/ImportUnityPackageImage.png">
</p>

This will add a number of directories to your project:

<p align="center">
  <img alt="Files included in the unity package"  width="500px" src="assets/VRSDKAssetsImage.png">
</p>

## Project settings

### Disable multi-threaded rendering

Open **Edit › Project Settings › Player**. In the Android tab, uncheck **Multithreaded Rendering**

<p align="center">
  <img alt="Uncheck multi-threaded rendering"  width="500px" src="assets/UncheckMultithreadedRenderingImage.png">
</p>

### Disable the splash screen

As the VR cameras only initialise after the splash screen has been displayed, the splash image does not display correctly in the headset.

If you are using the premium version of Unity, it is recommended to disable the splash screen and set the static splash image to a solid black image in **Project Settings**.

<p align="center">
  <img alt="Disable the splash screen" width="500px" src="assets/DisableSplashImage.png">
</p>

### Disable bundled Unity VR SDKs

Depending on the version of Unity you are using, the **Virtual Reality Supported** option can be found in **Other Settings** or **XR Settings**. Make sure it is **NOT** checked to avoid conflicts with the Pico VR SDK.

<p align="center">
  <img alt="Uncheck Virtual Reality Supported" width="500px" src="assets/DisabledVirtualRealitySupportImage.png">
</p>

## Quality Settings

Open **Edit › Project Settings › Quality** and change the following settings:

### Turn off vertical sync

When using Unity 5.4 or higher in the **Other** section, change **V sync Count** to **Don’t Sync**

<p align="center">
  <img alt="Turn off vertical sync" width="500px" src="assets/DisableVerticalSyncImage.png">
</p>

## AndroidManifest.xml file

If your project does not already have a `Assets/Plugins/Android/AndroidManifest.xml` file, you can use the one installed by the Pico SDK unity package.

If you already have an `AndroidManifest.xml` file in your project, you will need to manually merge in the values found in the unity package’s `AndroidManifest.xml`.

### Next: Enabling USB debugging

See [enabling USB debugging](/docs/pico-goblin-developer-mode-usb-debugging.md).
