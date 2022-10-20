---
layout: default-layout
title: Dynamsoft Capture Vision - Flutter Release Notes
description: This is the release notes of Dynamsoft Capture Vision - Flutter Edition.
keywords:  Capture Vision, Flutter, Release Notes
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: 1.x
---

# Release Notes for Flutter SDK - 1.x

## 1.1.0 (09/08/2022)

### New

- Added a new method [`decodeFile`](../api-reference/barcode-reader.md#decodefile) in Barcode Reader module to decode barcodes from an image file.
- Added a new method [`enableResultVerification`](../api-reference/barcode-reader.md#enableresultverification) in Barcode Reader module to further improve the accuracy of barcode result.
- Added a new property [`torchButton`](../api-reference/camera-view.md#torchbutton) to `DCVCameraView` class for users to create a torch button on the view.
- Added a new class [`Rect`](../api-reference/class-rect.md).
- Added a new property [`barcodeBytes`](../api-reference/class-barcode-result.md) in `BarcodeResult` to output the byte data of the barcode.
- Added a new property [`minResultConfidence`](../api-reference/class-dbr-runtime-settings.md) in `DBRRuntimeSettings` to filter the barcode results by confidence.
- Added a new property [`minResultTextLength`](../api-reference/class-dbr-runtime-settings.md) in `DBRRuntimeSettings` to filter the barcode results by text length.
- Added [`DCVCameraEnhancer`](../api-reference/camera-enhancer.md) class. Moved camera control APIs from `DCVCameraView` class to `DCVCameraEnhancer` class. Added a new method [`selectCamera`](../api-reference/camera-enhancer.md#selectcamera) in `DCVCameraEnhancer` class for users to switch between front-facing camera and back-facing camera.
- Added an enumeration [`EnumCameraPosition`](../api-reference/enum-camera-position.md).

### Changes

- Renamed `DynamsoftBarcodeReader` class to [`DCVBarcodeReader`](../api-reference/barcode-reader.md).
- Renamed `DynamsoftCameraView` class to [`DCVCameraView`](../api-reference/camera-view.md).
- Users have to call [`DCVCameraEnhancer.open`](../api-reference/camera-enhancer.md#open)/[`DCVCameraEnhancer.close`](../api-reference/camera-enhancer.md#close) manually when the application is **resumed**/**inactive**.

## 1.0.0 (07/12/2022)

{%- include release-notes/product-highlight-1.0.0.md -%}
