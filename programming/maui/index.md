---
layout: default-layout
title: Index - Dynamsoft Capture Vision MAUI Edition
description: The introduction of Dynamsoft Capture Vision MAUI edition.
keywords: API reference, index, MAUI
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Dynamsoft Capture Vision MAUI Edition - Documentation

Dynamsoft Capture Vision (DCV) is a comprehensive SDK that integrates various functional products. It encompasses image capture, content understanding, result parsing, and interactive workflow. Essentially, DCV processes images to extract specific information that is meaningful within a business context.

DCV is designed to enable developers to quickly create conceptual prototypes within hours. It also offers the flexibility to handle more complex customizations for demanding tasks.

> Read [Introduction to Dynamsoft Capture Vision]({{ site.dcvb_introduction }})

This documentation provides guidance to assist developers in utilizing DCV for MAUI applications.

## Using the SDK

### System Requirements

#### .Net

- .NET 8.0 and 9.0.

#### Android

- Supported OS: **Android 5.0** (API Level 21) or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Visual Studio 2022 recommended.
- JDK: 1.8+

#### iOS

- Supported OS: **iOS 11.0** or higher.
- Supported ABI: **arm64** and **x86_64**.
- Development Environment: Visual Studio 2022 for Mac and Xcode 14.3+ recommended.

### Get Started

- [Read Barcode]({{ site.dbr_maui }}user-guide.html)
- [Scan MRZ]({{ site.dcv_maui }}user-guide/mrz.html)
- [Detect & Normalize Documents]({{ site.ddn_maui }}user-guide.html)

### Check APIs

While the guide covers common APIs, more detailed explanations of these and other APIs can be found in the [API Reference](./api-reference/index.md).

### Read about CaptureVisionTemplate

Using DCV in MAUI involves:

1. Creating a `CaptureVisionRouter` instance.
2. Defining and binding an image source and a result receiver to the instance.
3. Specifying a template which defines how to process images.

Apparently, the use of DCV varies with the choice of template. Dynamsoft provides popular preset templates and will add more over time. To understand, adjust, or define your own template, read about [CaptureVisionTemplate]({{ site.parameter }}file/).

### Contact Us

Feel free to [contact us](https://www.dynamsoft.com/company/customer-service/#contact){:target="_blank"} if you have any questions.
