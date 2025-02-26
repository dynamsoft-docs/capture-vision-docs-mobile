---
layout: default-layout
title: Scan & Parse MRZ - Dynamsoft Capture Vision MAUI Edition
description: This page introduce how to scan and parse a MRZ with Dynamsoft Capture Vision MAUI Edition.
keywords: MAUI, MRZ, passport, id card, visa
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# MAUI User Guide for MRZ Scanner Integration

## Table of Contents

- [MAUI User Guide for MRZ Scanner Integration](#maui-user-guide-for-mrz-scanner-integration)
  - [Table of Contents](#table-of-contents)
  - [Supported Machine-Readable Travel Document Types](#supported-machine-readable-travel-document-types)
    - [ID (TD1 Size)](#id-td1-size)
    - [ID (TD2 Size)](#id-td2-size)
    - [Passport (TD3 Size)](#passport-td3-size)
  - [System Requirements](#system-requirements)
    - [.Net](#net)
    - [Android](#android)
    - [iOS](#ios)
  - [Installation](#installation)
    - [Visual Studio for Mac](#visual-studio-for-mac)
    - [Visual Studio for Windows](#visual-studio-for-windows)
  - [Build Your MRZ Scanner App](#build-your-mrz-scanner-app)
    - [Set up Development Environment](#set-up-development-environment)
    - [Initialize the Project](#initialize-the-project)
      - [Visual Studio](#visual-studio)
      - [Visual Studio for Mac](#visual-studio-for-mac-1)
    - [Include the Library](#include-the-library)
    - [Initialize MauiProgram](#initialize-mauiprogram)
    - [License Activation](#license-activation)
    - [Initialize the Capture Vision SDK](#initialize-the-capture-vision-sdk)
    - [Add the CameraView control in the Main Page](#add-the-cameraview-control-in-the-main-page)
    - [Open the Camera and Start Reading MRZ](#open-the-camera-and-start-reading-mrz)
    - [Obtaining Recognized Text Lines and Parsed MRZ](#obtaining-recognized-text-lines-and-parsed-mrz)
    - [Run the Project](#run-the-project)
  - [Licensing](#licensing)

## Supported Machine-Readable Travel Document Types

The Machine Readable Travel Documents (MRTD) standard specified by the International Civil Aviation Organization (ICAO) defines how to encode information for optical character recognition on official travel documents.

Currently, the SDK supports three types of MRTD:

> Note: If you need support for other types of MRTDs, our SDK can be easily customized. Please contact support@dynamsoft.com.

### ID (TD1 Size)

The MRZ (Machine Readable Zone) in TD1 format consists of 3 lines, each containing 30 characters.

<div>
   <img src="{{ site.dcvb_root }}programming/assets/td1-id.png" alt="Example of MRZ in TD1 format" width="60%" />
</div>

### ID (TD2 Size)

The MRZ (Machine Readable Zone) in TD2 format  consists of 2 lines, with each line containing 36 characters.

<div>
   <img src="{{ site.dcvb_root }}programming/assets/td2-id.png" alt="Example of MRZ in TD2 format" width="72%" />
</div>

### Passport (TD3 Size)

The MRZ (Machine Readable Zone) in TD3 format consists of 2 lines, with each line containing 44 characters.

<div>
   <img src="{{ site.dcvb_root }}programming/assets/td3-passport.png" alt="Example of MRZ in TD2 format" width="88%" />
</div>

## System Requirements

### .Net

- .NET 7.0, 8.0 and 9.0.

### Android

- Supported OS: **Android 5.0** (API Level 21) or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Visual Studio 2022 recommended.
- JDK: 1.8+

### iOS

- Supported OS: **iOS 11.0** or higher.
- Supported ABI: **arm64** and **x86_64**.
- Development Environment: Visual Studio 2022 for Mac and Xcode 14.3+ recommended.

## Installation

### Visual Studio for Mac

In the **NuGet Package Manager>Manage Packages for Solution** of your project, search for **Dynamsoft.CaptureVisionBundle.Maui** and **Dynamsoft.MRZ.Maui**. Select it and click **install**.

### Visual Studio for Windows

You have to Add the library via the project file and do some additional steps to complete the installation.

1. Add the library in the project file:

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">
        ...
        <ItemGroup>
            ...
            <PackageReference Include="Dynamsoft.CaptureVisionBundle.Maui" Version="2.6.1000" />
            <PackageReference Include="Dynamsoft.MRZ.Maui" Version="3.4.201" />
        </ItemGroup>
    </Project>
    ```

2. Open the **Package Manager Console** and run the following commands:

    ```bash
    dotnet build
    ```

> Note:
>
> - Windows system have a limitation of 260 characters in the path. If you don't use console to install the package, you will receive error "Could not find a part of the path 'C:\Users\admin\.nuget\packages\dynamsoft.imageprocessing.ios\2.4.200\lib\net7.0-ios16.1\Dynamsoft.ImageProcessing.iOS.resources\DynamsoftImageProcessing.xcframework\ios-arm64\dSYMs\DynamsoftImageProcessing.framework.dSYM\Contents\Resources\DWARF\DynamsoftImageProcessing'"
> - The library only support Android & iOS platform. Be sure that you remove the other platforms like Windows, maccatalyst, etc.

## Build Your MRZ Scanner App

Now you will learn how to create a SimpleMRZScanner using Dynamsoft Capture Vision MAUI SDK.

>Note:
>
> - You can get the similar source code of the SimpleMRZScanner app from the following link
>   - [C#](https://github.com/Dynamsoft/mrz-scanner-mobile-maui/tree/main/MRZScanner){:target="_blank"}.

### Set up Development Environment

If you are a beginner with MAUI, please follow the guide on the <a href="https://learn.microsoft.com/en-us/dotnet/maui/get-started/installation" target="_blank">.Net MAUI official website</a> to set up the development environment.

### Initialize the Project

#### Visual Studio

1. Open the Visual Studio and select **Create a new project**.
2. Select **.Net MAUI App** and click **Next**.
3. Name the project **SimpleMRZScanner**. Select a location for the project and click **Next**.
4. Select **.Net 7.0** and click **Create**.

#### Visual Studio for Mac

1. Open Visual Studio and select **New**.
2. Select **Multiplatform > App > .Net MAUI App > C#** and click **Continue**.
3. Select **.Net 7.0** and click **Continue**.
4. Name the project **SimpleMRZScanner** and select a location, click **Create**.

### Include the Library

Please view the [installation section](#installation) on how to add the library.

### Initialize MauiProgram

In **MauiProgram.cs**, add a custom handler for the `CameraView` control. Specifically, it maps the `CameraView` type to the `CameraViewHandler` type.

```c#
namespace SimpleMRZScanner;
using Microsoft.Extensions.Logging;
using Dynamsoft.CameraEnhancer.Maui;
using Dynamsoft.CameraEnhancer.Maui.Handlers;

public static class MauiProgram
{
    public static MauiApp CreateMauiApp()
    {
        var builder = MauiApp.CreateBuilder();
        builder
            .UseMauiApp<App>()
            .ConfigureFonts(fonts =>
            {
                fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
                fonts.AddFont("OpenSans-Semibold.ttf", "OpenSansSemibold");
            })
            .ConfigureMauiHandlers(handlers =>
            {
                handlers.AddHandler(typeof(CameraView), typeof(CameraViewHandler));
            });

#if DEBUG
        builder.Logging.AddDebug();
#endif

        return builder.Build();
    }
}
```

### License Activation

The Dynamsoft Capture Vision SDK needs a valid license to work. Please refer to the [Licensing](#licensing) section for more info on how to obtain a license.

Go to **MainPage.xaml.cs**. Add the following code to activate the license:

```c#
namespace SimpleMRZScanner;
using Dynamsoft.License.Maui;
using System.Diagnostics;

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

### Initialize the Capture Vision SDK

In the **MainPage.xaml.cs**, add the following code to initialize the Capture Vision SDK:

```c#
......
using Dynamsoft.CaptureVisionRouter.Maui;
using Dynamsoft.CameraEnhancer.Maui;
using Dynamsoft.Core.Maui;
using Dynamsoft.Utility.Maui;

public partial class MainPage : ContentPage, ILicenseVerificationListener, ICapturedResultReceiver
{
    CameraEnhancer enhancer;
    CaptureVisionRouter router;

    public MainPage()
    {
        ......

        // Create an instance of CameraEnhancer
        enhancer = new CameraEnhancer();
        // Create an instance of CaptureVisionRouter
        router = new CaptureVisionRouter();
        // Bind the router with the created CameraEnhancer
        router.SetInput(enhancer);
        // Add the result receiver to receive the textline result and parsed MRZ result
        router.AddResultReceiver(this);
        // Add the result filter to verify the result across multiple frames
        var filter = new MultiFrameResultCrossFilter();
        filter.EnableResultCrossVerification(EnumCapturedResultItemType.CRIT_TEXT_LINE, true);
        router.AddResultFilter(filter);
    }
}
```

### Add the CameraView control in the Main Page

In the **MainPage.xaml**, add a `CameraView` control:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:controls="clr-namespace:Dynamsoft.CameraEnhancer.Maui;assembly=Dynamsoft.CaptureVisionRouter.Maui"
             x:Class="SimpleMRZScanner.MainPage"
             Title="MainPage">
    <AbsoluteLayout>
        <controls:CameraView x:Name="cameraView"
                             AbsoluteLayout.LayoutBounds="0,0,1,1"
                             AbsoluteLayout.LayoutFlags="All"/>
    </AbsoluteLayout>
</ContentPage>
```

### Open the Camera and Start Reading MRZ

In this section, we are going to add code to start reading MRZ in the **MainPage.xaml.cs**.

```c#
......

public partial class MainPage : ContentPage, ILicenseVerificationListener, ICapturedResultReceiver, ICompletionListener
{
    ......
   protected override void OnHandlerChanged()
    {
        base.OnHandlerChanged();

        if (this.Handler != null)
        {
            enhancer.SetCameraView(cameraView);
        }
    }

    protected override async void OnAppearing()
    {
        base.OnAppearing();
        // Request camera permission
        await Permissions.RequestAsync<Permissions.Camera>();
        // Open camera
        enhancer?.Open();
        // Start reading MRZ
        router?.StartCapturing("ReadPassportAndId", this);
    }

    protected override void OnDisappearing()
    {
        base.OnDisappearing();
        // Close camera
        enhancer?.Close();
        // Stop reading MRZ
        router?.StopCapturing();
    }

    // It is called when StartCapturing is successful
    public void OnSuccess()
    {
        Debug.WriteLine("Success");
    }

    // It is called when StartCapturing is failed
    public void OnFailure(int errorCode, string errorMessage)
    {
        Debug.WriteLine(errorMessage);
    }
}
```

Open the **Info.plist** file under the **Platforms/iOS/** folder (Open with XML Text Editor). Add the following lines to request camera permission on iOS platform:

```xml
<key>NSCameraUsageDescription</key>
<string>The sample needs to access your camera.</string>
```

### Obtaining Recognized Text Lines and Parsed MRZ

In **MainPage.xaml.cs**, implement `ICapturedResultReceiver` to receive recognized text lines and parsed MRZ result in  `OnRecognizedTextLinesReceived` and `OnParsedResultsReceived` callback function.

```c#
......
using Dynamsoft.LabelRecognizer.Maui;
using Dynamsoft.CodeParser.Maui;

public partial class MainPage : ContentPage, ILicenseVerificationListener, ICapturedResultReceiver, ICompletionListener
{
    ......
    public void OnRecognizedTextLinesReceived(RecognizedTextLinesResult result)
    {
        if (result.Items == null)
        {
            return;
        }
        List<TextLineResultItem> items = result.Items;
        items.ForEach(item =>
        {
            text += item.Text + "\n\n";
        });
    }

    public void OnParsedResultsReceived(ParsedResult result)
    {
        if (result.Items == null)
            return;
        if (result.Items.Count() == 0)
        {
            if (text.Length != 0)
            {
                Debug.WriteLine("Error: Failed to parse the MRZ text: " + text);
            }
        }
        else
        {

            Dictionary<string, ParsedField> entry = result.Items[0].ParsedFields;
            string number = entry.ContainsKey("passportNumber") ? entry["passportNumber"].Value : entry.ContainsKey("documentNumber") ? entry["documentNumber"].Value : "";
            string firstName = entry.ContainsKey("secondaryIdentifier") ? " " + entry["secondaryIdentifier"].Value : "";
            string lastName = entry.TryGetValue("primaryIdentifier", out var identifier) ? identifier.Value ?? "" : "";
            string name = lastName + firstName;
            // Process the results according to your needs.

            Debug.WriteLine("MRZ Result:\n" + "Number:" + number + "\nName:" + name);
        }
    }
}
```

### Run the Project

Select your device and run the project.

You can get the similar source code of the SimpleMRZScanner app from the following link:

- [C#](https://github.com/Dynamsoft/mrz-scanner-mobile-maui/tree/main/MRZScanner){:target="_blank"}.

> Note: If you are running Android only on Visual Studio Windows, please manually exclude iOS and Windows platforms. Otherwise, the Visual Studio will report type or namespace not found errors.

![Exclude iOS and Windows from targets](../assets/maui-exclude.png)

## Licensing

- A one-day trial license is available by default for every new device to try Dynamsoft Capture Vision SDK.
- You can request a 30-day trial license via the [Request a Trial License](https://www.dynamsoft.com/customer/license/trialLicense?product=dcv&package=mobile&utm_source=docs){:target="_blank"} link.
- [Contact us](https://www.dynamsoft.com/company/contact/){:target="_blank"} to purchase a full license.
