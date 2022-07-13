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

### Xamarin & Dart

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

## Build Your Barcode Scanner App

Now you will learn how to create a simple barcode scanner using Dynamsoft Capture Vision Xamarin SDK.

### Set up Development Environment

### Initialize the Project

### Include the Library

View the [installation section](#installation) on how to add the library.

### License Activation

The barcode reading module of Dynamsoft Capture Vision needs a valid license to work. Please refer to the [Licensing](#licensing) section for more info on how to obtain a license.

```c#
```

### Configure the Barcode Reader

### Build the Widget

### Configure Camera Permissions

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
