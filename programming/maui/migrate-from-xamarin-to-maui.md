---
layout: default-layout
title: Migrate from Xamarin Forms to MAUI - Dynamsoft Document Normalizer for MAUI
description: This is the migration guide from Xamarin Forms to MAUI for the Dynamsoft Document Normalizer
keywords: user guide, maui, xamarin forms, document normalizer
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# How to migrate from Xamarin Forms to MAUI

Previously, the Dynamsoft Document Normalizer (DDN) was available for the Xamarin.Forms platform - allowing users to integrate document scanning and image capture capabilities into their Xamarin apps. With the [retirement of Xamarin by Microsoft](https://dotnet.microsoft.com/en-us/platform/support/policy/xamarin), we recommend that all of our DDN Xamarin users move to MAUI to make use of the latest features of DDN. With the most recent Dynamsoft Capture Vision release, the Dynamsoft Document Normalizer SDK has been refactored to align with the [DynamsoftCaptureVision (DCV)]({{ site.architecture }}) architecture. This guide will help you migrate from your old Xamarin DDN app to a new MAUI DDN app as quickly as possible. We recommend following the [User Guide]({{ site.ddn_maui }}user-guide.html) and re-writing your code accordingly.

## Updating the Project

Previously, you created a Mobile App (Xamarin.Forms) project. Now, you’ll need to create a standalone .NET MAUI App project. For more info on this, please follow the [user guide]({{ site.ddn_maui }}user-guide.html#initialize-the-project).

## Updating the Library

In your Xamarin.Forms project, you added the **Dynamsoft.DocumentNormalizer.Xamarin.Forms** library. Now, in your MAUI project, you’ll need to use the **Dynamsoft.CaptureVisionBundle.Maui** library. Please refer to the [User Guide]({{ site.ddn_maui }}user-guide.html#installation) for further instructions.

## Update the License Activation Code

Starting from 2.4.2000, we have unified the API for setting licenses across different Dynamsoft products.

| Old APIs | New APIs |
| :----------- | :------- |
| `ILicenseManager.InitLicense` | `LicenseManager.InitLicense` |

### Code in Xamarin.Forms

```c#
public partial class App : Application, ILicenseVerificationListener
{
    public static ICameraEnhancer dce;
    public static IDocumentNormalizer ddn;
    public static ILicenseManager licenseManager;

    public App(ICameraEnhancer enhancer, IDocumentNormalizer normalizer, ILicenseManager manager)
    {
        InitializeComponent();
        dce = enhancer;
        ddn = normalizer;
        licenseManager = manager;
        licenseManager.InitLicense("Put your license here.", this);
        MainPage = new NavigationPage(new MainPage());
    }

    public void LicenseVerificationCallback(bool isSuccess, string msg)
    {
        // code to deal with the license verification
    }
}
```

### Code in MAUI

```c#
public partial class MainPage : ContentPage, ILicenseVerificationListener
{
    public MainPage()
    {
        InitializeComponent();
        LicenseManager.InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", this);
    }
    public void OnLicenseVerified(bool isSuccess, string message)
    {
        if (!isSuccess)
        {
            Debug.WriteLine(message);
        }
    }
}
```

## Update Video Streaming Decoding APIs

The APIs for decoding video frames has been adjusted as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `IDocumentNormalizer.SetCameraEnhancer` | `CaptureVisionRouter.SetInput` |
| `IDocumentNormalizer.StartDetecting` | `CaptureVisionRouter.StartCapturing` |
| `IDocumentNormalizer.StopDetecting` | `CaptureVisionRouter.StopCapturing` |
| `IDocumentNormalizer.AddResultListener` | `CaptureVisionRouter.addResultReceiver` |
| `interface IDetectResultListener` | `interface ICapturedResultReceiver` |
| `class NormalizedImageResult` | `class NormalizedImageResultItem` |
| `class DetectedQuadResult` | `class DetectedQuadResultItem` |

## Migrate Your Templates

The template format has changed in the latest version of the Document Normalizer. The template you used for the previous version cannot be used by the new version. If you are using a settings template, please <a href="https://download2.dynamsoft.com/dcv/TemplateConverter.zip" target="_blank">download the TemplateConverter tool (Windows only)</a> or <a href="https://www.dynamsoft.com/company/customer-service/#contact" target="_blank">contact us</a> to upgrade your template.

The template-based APIs have been updated as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `IDocumentNormalizer.InitRuntimeSettings` | `CaptureVisionRouter.InitSettings` or `CaptureVisionRouter.InitSettingsFromFileAsync` |
| `IDocumentNormalizer.InitRuntimeSettingsFromFile` | `CaptureVisionRouter.InitSettingsFromFile` or `CaptureVisionRouter.InitSettingsFromFileAsync` |
| `IDocumentNormalizer.OutputRuntimeSettings` | `CaptureVisionRouter.OutputSettings` |
