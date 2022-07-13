---
layout: default-layout
title: The index of Xamarin API Reference
description: This page is the index of Xamarin API reference
keywords: API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: API Index
---

# Xamarin API Reference

## Name Space DCVXamarin

### Primary Classess/Interfaces

| Classes | Description |
| ------- | ----------- |
| [`IBarcodeReader`](barcode-reader.md) | The interface that contains barcode decoding related APIs. |
| [`ICameraEnhancer`](camera-enhancer.md) | The interface that contains camera control and camera enhancements related APIs. |
| [`CameraView`](camera-view.md) | The class that helps you deploy a camera view for displaying and processing the video stream. You can also add basic UI elements on the view. |

### Auxiliary Classess/Interfaces

| Classes | Description |
| ------- | ----------- |
| [`Region`](class-region.md) | The class that stores the region information. Users can configure region of interest. |
| [`Quadrilateral`](class-quadrilateral.md) | The class that stores the vertex coordinates of the quadrilateral.|
| [`BarcodeResult`](class-barcode-result.md) | The class that stores the barcode results. Barcode result can be acquired from result callback when using video barcode decoding. |
| [`BarcodeLocationResult`](class-barcode-location-result.md) | The class that stores the location result of the detected barcodes. |
| [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) | The class that stores barcode decoding settings. |
| [`TorchButton`](class-torch-button.md) | The class stores the torch button configurations. |
| [`ILicenseVerificationListener`](interface-license-verification-listener.md) | The listener for users to receive license verification message from the license server. |
| [`IBarcodeResultListener`](interface-barcode-result-listener.md) | The listener for users to receive the decoded barcode results. |

### Enumerations

| Enumerations | Description |
| ------------ | ----------- |
| [`EnumBarcodeFormat`](enum-barcode-format.md) | The enumeration stores the first group of barcode formats. |
| [`EnumBarcodeFormat_2`](enum-barcode-format2.md) | The enumeration stores the second group of barcode formats. |
| [`EnumDBRPresetTemplate`](enum-dbr-preset-template.md) | The enumeration stores the preset barcode decoding templates. |

## Name Space DCVXamarin.Droid

| Classes | Description |
| ------- | ----------- |
| [`CameraEnhancer`](camera-enhancer.md) | Implements ICameraEnhancer on Android. |
| [`BarcodeRader`](barcode-reader.md) | Implements IBarcodeReader on Android. |

## Name Space DCVXamarin.iOS

| Classes | Description |
| ------- | ----------- |
| [`CameraEnhancer`](camera-enhancer.md) | Implements ICameraEnhancer on iOS. |
| [`BarcodeRader`](barcode-reader.md) | Implements IBarcodeReader on iOS. |
