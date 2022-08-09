---
layout: default-layout
title: Getting Started with Barcode Reader
description: This is the user guide of Dynamsoft Capture Vision Cordova edition - Barcode Reader module
keywords: User guide, Barcode Reader, Cordova, Capture Vision, Dynamsoft
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Guide of Dynamsoft Barcode Reader Cordova
---

# Barcode Reader User Guide for Cordova

In this guide, we will explore the Barcode Reader module of the Dynamsoft Capture Vision library for Cordova.

## Table of Contents

- [Barcode Reader User Guide for Cordova](#barcode-reader-user-guide-for-cordova)
  - [Table of Contents](#table-of-contents)
  - [System Requirements](#system-requirements)
    - [Cordova](#cordova)
    - [Android](#android)
    - [iOS](#ios)
  - [Installation](#installation)
  - [Build Your Barcode Scanner App](#build-your-barcode-scanner-app)
    - [Set up Development Environment](#set-up-development-environment)
    - [Initialize the Project](#initialize-the-project)
    - [Include the Library](#include-the-library)
    - [Add Camera Permission](#add-camera-permission)
      - [Android](#android-1)
      - [iOS](#ios-1)
    - [Run the Project](#run-the-project)
      - [Run Android on Windows](#run-android-on-windows)
      - [Run iOS & Android on macOS](#run-ios--android-on-macos)
  - [Customizing the Barcode Reader](#customizing-the-barcode-reader)
    - [Using the Settings Templates](#using-the-settings-templates)
    - [Using the DBRRuntimeSettings Interface](#using-the-dbrruntimesettings-interface)
    - [Customizing the Scan Region](#customizing-the-scan-region)
  - [Licensing](#licensing)

## System Requirements

### Cordova

### Android

### iOS

## Installation

- Install from GitHub

```bash
cordova plugin add https://github.com/Dynamsoft/capture-vision-cordova
```

- Install from npm

```bash
cordova plugin add dynamsoft-capture-vision-cordova
```

## Build Your Barcode Scanner App

Now you will learn how to create a simple barcode scanner using Dynamsoft Capture Vision Cordova SDK.

>Note: You can get the full source code of a similar project: <a href="https://github.com/Dynamsoft/capture-vision-cordova-samples/tree/main/BarcodeReaderSimpleSample" target="_blank">Barcode Reader Simple Sample</a>.

### Set up Development Environment

If you are a beginner with Cordova, please follow the guide on the <a href="" target="_blank">Cordova official website</a> to set up the development environment.

### Initialize the Project

Use the following command to create a new project.

```bash
cordova create SimpleBarcodeScanner
```

### Include the Library

```bash
cordova plugin add dynamsoft-capture-vision-cordova
```

### Add Camera Permission

#### Android

#### iOS

Add **Privacy - Camera Usage Description** and your message to the **info.plist** of your project.

### Run the Project

#### Run Android on Windows

#### Run iOS & Android on macOS

## Customizing the Barcode Reader

### Using the Settings Templates

DBR offers several preset templates for different popular scenarios. For example, to prioritize speed over accuracy, you can use one of the speed templates and choose the corresponding template for images or video, and vice versa if you’re looking to prioritize read rate and accuracy over speed. For the full set of templates, please refer to `EnumPresetTemplate`. Here is a quick example of prioritizing read rate for image-based decoding:

```js
```

### Using the DBRRuntimeSettings Interface

The SDK also supports a more granular control over the individual runtime settings rather than using a preset template. The main settings that you can control via this interface are which barcode formats to read, the expected number of barcodes to be read in a single image or frame, and the timeout. For more info on each, please refer to `DBRRuntimeSettings`. Here is a quick example:

```js
```

### Customizing the Scan Region

You can also limit the scan region of the SDK so that it doesn’t exhaust resources trying to read from the entire image or frame. In order to do this, we will need to use the `Region` class as well as the `DCVCameraEnhancer` class.

How to set scan region:

- Define a `Region` object via class Region.
- Configure the value of `Region`.
- Assign the `Region` to the `ScanRegion` property of the `IDCVCameraEnhancer` object.

```js
```

## Licensing

- The `BarcodeReader` module of Dynamsoft Capture Vision needs a valid license to work.
- A one-day trial license is available by default for every new device to try Dynamsoft Capture Vision.
- You can <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=dbr&package=mobile&utm_source=docs" target="_blank"> request a 30-day free trial license</a> via Dynamsoft customer portal for further evaluation.
- [Contact us](https://www.dynamsoft.com/company/contact/) to purchase a full license.
