---
layout: default-layout
title: Index - Dynamsoft Capture Vision iOS Edition
description: The introduction of Dynamsoft Capture Vision iOS edition.
keywords: API reference, index, iOS
needAutoGenerateSidebar: true
noTitleIndex: false
---

# Dynamsoft Capture Vision iOS Edition - Documentation

Dynamsoft Capture Vision (DCV) is a comprehensive SDK that integrates various functional products. It encompasses image capture, content understanding, result parsing, and interactive workflow. Essentially, DCV processes images to extract specific information that is meaningful within a business context.

DCV is designed to enable developers to quickly create conceptual prototypes within hours. It also offers the flexibility to handle more complex customizations for demanding tasks.

> Read [Introduction to Dynamsoft Capture Vision]({{ site.dcvb_introduction }})

This documentation provides guidance to assist developers in utilizing DCV for iOS applications.

## Using the SDK

### System Requirements

- Supported OS: iOS 11+ (iOS 13+ recommended).
- Supported ABI: arm64 and x86_64.
- Development Environment: Xcode 13+ (Xcode 14.1+ recommended).

### Get Started

- [Read Barcode]({{ site.dbr_ios }}user-guide.html)
- [Scan MRZ]({{ site.dcv_ios }}user-guide/mrz.html)
- [Detect & Normalize Documents]({{ site.ddn_ios }}user-guide.html)

### Check APIs

While the guide covers common APIs, more detailed explanations of these and other APIs can be found in the [API Reference](./api-reference/index.md).

### Read about CaptureVisionTemplate

Using DCV in iOS involves:

1. Creating a `CaptureVisionRouter` instance.
2. Defining and binding an image source and a result receiver to the instance.
3. Specifying a template which defines how to process images.

Apparently, the use of DCV varies with the choice of template. Dynamsoft provides popular preset templates and will add more over time. To understand, adjust, or define your own template, read about [CaptureVisionTemplate]({{ site.parameter }}file/).

### Contact Us

Feel free to [contact us](https://www.dynamsoft.com/company/customer-service/#contact){:target="_blank"} if you have any questions.
