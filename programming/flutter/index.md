---
layout: default-layout
title: Dynamsoft Barcode Reader Flutter API Reference - Main Page
description: This is the main page of Dynamsoft Barcode Reader SDK API Reference for Flutter.
keywords: api reference, Flutter, barcode reader
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Capture Vision SDK Overview: Modules and Main APIs

This page provides an overview of the various modules and highlights the most essential APIs that form Dynamsoft Capture Vision, the backbone of Dynamsoft Barcode Reader SDKs.

## Modules Summary

**dynamsoft_capture_vision_flutter** represents the Dynamsoft Capture Vision library - the parent library that contains the foundational classes and methods for not only the Barcode Reader, but the other functional Dynamsoft products such as the Dynamsoft Label Recognizer and the Dynamsoft Document Normalizer.

**dynamsoft_barcode_reader_bundle_flutter** is built on the Dynamsoft Capture Vision (DCV) framework, which includes multiple modules working together to achieve the full barcode reading functionality. This library gives the developer access to the `BarcodeScanner` class, a **ready-to-use barcode reader** that requires minimal effort and configuration and comes with a sophisticated and user-friendly UI.

The hierarchical structure diagram below illustrates the various modules of the Barcode Reader SDK (with modules at the top depending on those below).

<div align="center">
    <p><img src="../../assets/dcv-dependencies.png" width="70%" alt="dcv-dependencies"></p>
    <p>Modules hierarchical of the DBR SDK</p>
</div>

## API Overview

### Capture Vision Router

The Dynamsoft Capture Vision Router class is the cornerstone of the Dynamsoft Capture Vision (DCV) architecture. It focuses on coordinating batch image processing and provides API for setting up image sources and result receivers, configuring workflows with parameters, and controlling processes. Dynamsoft Capture Vision helps connects the functional products of Dynamsoft under the same umbrella - allowing for easier integration and interchangeable API to control them all.

You can find the CaptureVisionRouter API [here](./api-reference/capture-vision-router/capture-vision-router.md).

This guide focuses on the Barcode Reader functional product. To learn how to use the foundational Capture Vision API to set up and run the Barcode Reader, please refer to the [User Guide (Foundational Edition)]({{ site.dbr_flutter }}foundational-user-guide.html).

### Barcode Reader

The Barcode Reader can be implemented by two sets of API - each offering a different experience. 

#### BarcodeScanner Edition

The first (and recommended) way is to use the BarcodeScanner API - which comes with a ready-to-use UI and a simpler configuration setup, allowing the developer to quickly and easily integrate barcode scanning into their Flutter app. The BarcodeScanner API uses the foundational Capture Vision API as a basis, but comes with its own API to allow for an easier development process. To learn more about the BarcodeScanner API, please visit the [BarcodeScanner API Reference page]({{ site.dbr_flutter_api }}barcode-scanner/index.html).

> [!TIP]
> To learn how to implement the Barcode Reader using the BarcodeScanner API, please read through the [Barcode Reader Integration Guide (Ready-To-Use Edition)]({{ site.dbr_flutter }}user-guide.html).

#### Foundational Edition

The alternative is to use the foundational Capture Vision API directly. Even though using the foundational API is a bit more complicated than the ready-to-use BarcodeScanner API, the foundational API allows for more intricate control over the Barcode Reader configuration and settings. With this implementation, you will lose the ready-to-use UI, but in scenarios where the developer has their own customized UI, this could prove beneficial.

> [!TIP]
> To learn how to implement the Barcode Reader using the foundational API, please read through the [Barcode Reader Integration Guide (Foundational Edition)]({{ site.dbr_flutter }}foundational-user-guide.html).
