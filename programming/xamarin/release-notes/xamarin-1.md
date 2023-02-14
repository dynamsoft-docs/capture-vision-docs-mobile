---
layout: default-layout
title: Dynamsoft Capture Vision - Xamarin Release Notes
description: This is the release notes of Dynamsoft Capture Vision - Xamarin Edition.
keywords:  Capture Vision, Xamarin, Release Notes
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: 1.x
---

# Release Notes for Xamarin SDK - 1.x

## 1.0.3 (02/14/2023)

- Fixed a crash bug on the devices that do not support 16:9 size resolution.

## 1.0.2 (12/20/2022)

- Added [`ScanRegionVisile`](../api-reference/camera-enhancer.md#scanregionvisible) in interface `IDCVCameraEnhancer` so that users can hide the **scan region** on the UI.
- Added a new method [`EnableResultVerification`](../api-reference/barcode-reader.md#enableresultverification) in interface `IDCVBarcodeReader` to improve the accuracy of barcode results for video streaming barcode decoding.
- Added new methods [`EnableDuplicateFilter`](../api-reference/barcode-reader.md#enableduplicatefilter) and [`DuplicateForgetTime`](../api-reference/barcode-reader.md#duplicateforgettime) in interface `IDCVBarcodeReader` to filter out the duplicate results in a period of time for video barcode decoding.
- Added [`MinImageReadingInterval`](../api-reference/barcode-reader.md#minimagereadinginterval) to set the minimum interval between two barcode decoding.
- Added two new parameters `MinResultConfidence` and `MinBarcodeTextLength` in class [`DBRRuntimeSettings`](../api-reference/class-dbr-runtime-settings.md) to filter out unqualified barcode results.

## 1.0.1 (10/17/2022)

- Fixed a duplicate symbol issue.

## 1.0.0 (08/04/2022)

### HighLights

{%- include release-notes/product-highlight-1.0.0.md -%}
