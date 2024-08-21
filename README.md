# Microgestures Toolkit for HoloLens

## Introduction
The primary aim of this toolkit is to facilitate the integration of hand microgestures into augmented reality (AR) applications, catering specifically to researchers and developers in the field. It is designed to bridge the gap between complex gesture recognition capabilities and user-friendly AR experiences, enabling advanced interaction models within mixed reality environments. By providing an accessible framework for recognizing and implementing microgestures, this toolkit opens up new avenues for interaction design and research, allowing for the creation of more intuitive and immersive AR applications. Whether you're looking to conduct research in human-computer interaction, develop cutting-edge AR content, or explore the possibilities of microgestures in mixed reality, this toolkit is tailored to update and empower your projects with the latest advancements in gesture recognition technology.

## Features
- Hand microgestures supported

## Prerequisites
Before you begin, ensure you have the following:
- Unity 2020.3 LTS or newer.
- Mixed Reality Feature Tool ( [link here](https://www.microsoft.com/en-us/download/details.aspx?id=102778) )
- A HoloLens 2 device or emulator for testing.

## Installation

## Step 1: Clone or Download the repository

## Step 2: Create a 3D Project in Unity
- Open Unity Hub and create a new 3D project. Name it appropriately.

## Step 3: Configure Mixed Reality
- Using the Mixed Reality Feature Tool, browse to the project you created.
- Install the following packages from the **Mixed Reality Toolkit Section** (note: do not use MRTK3):
  - Mixed Reality Toolkit Extensions
  - Mixed Reality Toolkit Foundations
  - Mixed Reality Toolkit Standard Assets

## Step 4: Install the OpenXR Plugin
- In the **Platform Support** section of the Mixed Reality Feature Tool, select the **OpenXR Plugin**.
- Validate and import the features into your Unity project.

## Step 5: Prepare the Assets Folder
- In your Unity project, clear out everything found in the `Assets` folder.
- Copy and paste the entire toolkit's files, or drag and drop them into the `Assets` folder.

## Step 6: Configure Project Settings
- Navigate to `Project Settings > OpenXR`.
- Add the following to the enabled interaction profiles:
  - Hand Interaction Profile
  - Eye Gaze Interaction Profile
  - Microsoft Hand Interaction Profile
- Ensure the following are checked under **Open XR Features Groups**:
  - Microsoft HoloLens
- To the right side make sure these are checked:
  - Hand Interaction Poses
  - Hand Tracking

## Step 7: Verify Artefacts and Representations
- Check that the artefacts and representations are displaying correctly:
  - Artefacts can be found under `Assets > uRepToolkit > Prefabs > Artefacts > AandB`.
  - Representations are located at `Assets > uRepToolkit > Prefabs > Representations`.

## Step 8: Setup MixedRealityToolkit Component
- In the `MainScene`, ensure that the `MixedRealityToolkit` component references the MixedRealityToolkit script in the inspector.

## Step 9: Configure uRepToolkit
- Click on the `uRepToolkit` object.
- Ensure the `uRepToolkit` script is assigned to it.
- Here, you can assign multiple representations that will appear when running the project.


## Potential Risks and Solutions

### 1. **Network Connectivity Issues**

**Risk**: Failure to connect to HoloLens over the network, leading to errors such as failure to deploy or start debugging sessions.

**Solution**:
- Ensure both the PC and HoloLens are on the same network.
- Disable VPNs and ensure no firewall settings are blocking the connection.
- Verify that the IP address configured in Visual Studio matches the HoloLens device IP.
- Use command prompt to ping the HoloLens IP to check connectivity.

### 2. **Configuration Errors**

**Risk**: Incorrect project configuration in Unity or Visual Studio can prevent successful deployment.

**Solution**:
- Double-check Unity Build Settings, ensuring the target is set to Universal Windows Platform (UWP) and the correct SDK is selected.
- In Visual Studio, ensure the target device is set properly (Device for USB, Remote Machine for IP).
- Validate that the correct architecture (x86 for HoloLens 1, ARM64 for HoloLens 2) is selected.

### 3. **Software Version Compatibility**

**Risk**: Incompatibility between Unity, Visual Studio, or HoloLens OS versions can cause deployment failures.

**Solution**:
- Update Unity, Visual Studio, and HoloLens to their latest supported versions.
- Check Microsoft's official documentation for compatible versions.

### 4. **Visual Studio Deployment Errors**

**Risk**: Errors like DEP6701 indicating issues with the bootstrapping process due to null or empty parameters.

**Solution**:
- Reconfirm all deployment settings in Visual Studio, especially the target device and IP address.
- Restart Visual Studio and the HoloLens to refresh connections and settings.
- Use Visual Studio’s diagnostic tools to get more detailed error logs.

### 5. **USB Connection Failures**

**Risk**: USB deployment fails due to poor connection or unrecognized device.

**Solution**:
- Ensure a reliable USB connection between the PC and HoloLens.
- Check Device Manager on the PC to see if the HoloLens is recognized.
- Try a different USB port or cable if problems persist.

### 6. **Firewall and Antivirus Interference**

**Risk**: Security software on your PC may interfere with network traffic or the deployment process.

**Solution**:
- Temporarily disable antivirus and firewall software during deployment.
- Add exceptions for Visual Studio and the HoloLens in the security software settings.

## Additional Tips

- Regularly back up your project.
- Maintain a log of any changes to configuration or software versions.
- Consult Microsoft’s official forums or support for unresolved issues.

---

Happy building! Enjoy creating immersive mixed reality experiences with [Your Toolkit Name].

