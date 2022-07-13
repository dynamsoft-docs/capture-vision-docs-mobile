---
layout: default-layout
title: Getting Started with Barcode Reader
description: This is the user guide of Dynamsoft Capture Vision Xamarin edition - Barcode Reader module
keywords: User guide, Barcode Reader, Xamarin, Capture Vision, Dynamsoft
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Guide of Dynamsoft Barcode Reader Xamarin
---

# Barcode Reader User Guide for Xamarin

In this guide, we will explore the Barcode Reader module of the Dynamsoft Capture Vision library for Xamarin.

## Table of Contents

- [System Requirements](#system-requirements)
- [Installation](#installation)
- [Build Your Barcode Scanner App](#build-your-barcode-scanner-app)
  - [Set up Development Environment](#set-up-development-environment)
  - [Initialize the Project](#initialize-the-project)
  - [Include the Library](#include-the-library)
  - [License Activation](#license-activation)
  - [Configure the Barcode Reader](#configure-the-barcode-reader)
  - [Build the Widget](#build-the-widget)
  - [Configure Camera Permissions](#configure-camera-permissions)
  - [Run the Project](#run-the-project)
- [Customizing the Barcode Reader](#customizing-the-barcode-reader)
  - [Using the Settings Templates](#using-the-settings-templates)
  - [Using the DBRRuntimeSettings Interface](#using-the-dbrruntimesettings-interface)
  - [Customizing the Scan Region](#customizing-the-scan-region)
- [Licensing](#licensing)

## System Requirements

### Xamarin

- NETStandard.Library 2.0+
- Xamarin.Essentials
- Xamarin.Forms

### Android

- Supported OS: Android 5.0 (API Level 21) or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Android Studio 3.4+ (Android Studio 4.2+ recommended).
- JDK: 1.8+

### iOS

- Supported OS: **iOS 10.0** or higher.
- Supported ABI: **arm64** and **x86_64**.
- Development Environment: Xcode 7.1 and above (Xcode 13.0+ recommended), CocoaPods 1.11.0+.

## Installation

In the **NuGet Package Manager** of your project, search for **DCVXamarin** and install the package.

## Build Your Barcode Scanner App

Now you will learn how to create a simple barcode scanner using Dynamsoft Capture Vision Xamarin SDK.

### Set up Development Environment

If you are a beginner with Xamarin, please follow the guide on the <a href="https://dotnet.microsoft.com/en-us/learn/xamarin/hello-world-tutorial/install" target="_blank">Xamarin official website</a> to set up the development environment.

### Initialize the Project

1. Open the Visual Studio and select **Create a new project**.
2. Select **Mobile App (Xamarin.Forms)** and click **Next**.
3. Here we name the project **SimpleBarcodeScanner**. Select a location for the project and click **Create**.
4. Select Blank and click **Create**.

### Include the Library

Add NuGet package **DCVXamarin** to your project. You can view the [installation section](#installation) on how to add the library.

### Initialize IBarcodeReader and ICameraEnhancer

You have to initialize the follow two interfaces to decode barcodes with the library.

- `IBarcodeReader`: The interface that defines barcode decoding APIs. This is the interface to set up barcode decoding configurations.
- `ICameraEnhancer`: The interface that defines camera controlling APIs. This is the module for you to set up a camera module to capture video stream.

In **App.xaml.cs**, add the following code to initialize the IBarcodeReader and ICameraEnhancer.

```c#
namespace SimpleBarcodeScanner
{
    public partial class App : Application, ILicenseVerificationListener
    {
        public static ICameraEnhancer Camera;
        public static IBarcodeReader BarcodeReader;
        public App(ICameraEnhancer dce, IBarcodeReader dbr)
        {
            InitializeComponent();
            Camera = dce;
            BarcodeReader = dbr;

            MainPage = new MainPage();
        }
    }
}
```

#### Implement the Interfaces for Android

Open the **MainActivity.cs** in **SimpleBarcodeScanner.Android** folder. Change the code of `LoadApplication` to:

```c#
LoadApplication(new App(new CameraEnhancer(), new BarcodeReader()));
```

#### Implement the Interfaces for iOS

Open the **AppDelegate.cs** in **SimpleBarcodeScanner.iOS** folder. Change the code of `LoadApplication` to:

```c#
LoadApplication(new App(new CameraEnhancer(), new BarcodeReader()));
```

### License Activation

The barcode reading module of Dynamsoft Capture Vision needs a valid license to work. Please refer to the [Licensing](#licensing) section for more info on how to obtain a license.

Go back to **App.xaml.cs**. Add the following code to activate the license:

```c#
namespace SimpleBarcodeScanner
{
    // Add ILicenseVerificationListener to the class and implement LicenseVerificationCallback.
    public partial class App : Application, ILicenseVerificationListener
    {
        public App(ICameraEnhancer dce, IBarcodeReader dbr)
        {
            ...
            // Initialize the license of barcode reader module.
            BarcodeReader.InitLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", this);
            ...
        }

        // Implement LicenseVerificationCallback to get message from the license server.
        public void LicenseVerificationCallback(bool isSuccess, string msg)
        {
            if (!isSuccess)
            {
                System.Console.WriteLine(msg);
            }
        }
    }
}

```

### Configure the Barcode Reader

In this section, we are going to add configurations for barcode decoding in the **MainPage** of the project.

#### Setup the Barcode Decoding Thread

Open the MainPage.xaml.cs and add the following code:

```c#
namespace SimpleBarcodeScanner
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            // Bind the CameraEnhancer to the BarcodeReader so that it can continuously obtain video stream from the camera for barcode decoding.
            App.BarcodeReader.SetCameraEnhancer(App.Camera);
        }

        protected override void OnAppearing()
        {
            base.OnAppearing();
            // Open the camera the the view appears.
            App.Camera.Open();
            // Start barcode decoding thread when the view appears.
            App.BarcodeReader.StartScanning();
        }

        protected override void OnDisappearing()
        {
            base.OnDisappearing();
            // Close the camera the the view appears.
            App.Camera.Close();
            // Stop barcode decoding thread when the view appears.
            App.BarcodeReader.StopScanning();
        }
    }
}
```

#### Receive and Display the Results

```c#
namespace SimpleBarcodeScanner
{
    // Add IBarcodeResultListener to your MainPage so that you can receive the barcode results.
    public partial class MainPage : ContentPage, IBarcodeResultListener
    {
        public MainPage()
        {
            ...
            App.BarcodeReader.AddResultlistener(this);
        }
        ...
        // Implement the BarcodeResultCallback so that you can receive the barcode results when the barcodes are decoded.
        public void BarcodeResultCallback(int frameID, BarcodeResult[] barcodeResults)
        {
            // Here is an example code on how to display the barcode results on the view.
            string newBarcodeText = "";
            if (barcodeResults != null && barcodeResults.Length>0)
            {
                for (int i=0; i<barcodeResults.Length; i++)
                {
                    {
                        newBarcodeText += barcodeResults[i].BarcodeText;
                        newBarcodeText += "; ";
                    }
                }
                Device.BeginInvokeOnMainThread(()=> {
                    barcodeResultLabel.Text = newBarcodeText;
                });
            }
        }
    }
}
```

### Configure the CameraView

### Run the Project

#### Run Android on Windows

#### Run iOS on macOS

## Customizing the Barcode Reader

### Using the Settings Templates

DBR offers several preset templates for different popular scenarios. For example, to prioritize speed over accuracy, you can use one of the speed templates and choose the corresponding template for images or video, and vice versa if you’re looking to prioritize read rate and accuracy over speed. For the full set of templates, please refer to `EnumPresetTemplate`. Here is a quick example:

```c#
```

### Using the DBRRuntimeSettings Interface

The SDK also supports a more granular control over the individual runtime settings rather than using a preset template. The main settings that you can control via this interface are which barcode formats to read, the expected number of barcodes to be read in a single image or frame, and the timeout. For more info on each, please refer to `DBRRuntimeSettings`. Here is a quick example:

```c#
```

### Customizing the Scan Region

You can also limit the scan region of the SDK so that it doesn’t exhaust resources trying to read from the entire image or frame. In order to do this, we will need to use the `Region` class as well as the `ICameraEnhancer` component.

How to set scan region:

- Define a `Region` object via class Region.
- Configure the value of `Region`.
- Use the `Region` you created as the parameter to active `SetScanRegion` method of `ICameraEnhancer`.

```c#
```

## Licensing

- The `BarcodeReader` module of Dynamsoft Capture Vision needs a valid license to work.
- A time-limited public trial license is available for every new device for the first use of Dynamsoft Capture Vision.
- If your public trial key is expired, please visit <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=dbr&utm_source=docs" target="_blank">Private Trial License Page</a> to get a 30-day trial extension.
- [Contact Us](https://www.dynamsoft.com/company/contact/) to purchase a full license.
