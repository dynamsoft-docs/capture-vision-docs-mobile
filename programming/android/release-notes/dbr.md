---
layout: default-layout
title: DBR Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of DynamsoftBarcodeReader module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, barcode reader, Android, DBR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftBarcodeReader Module

## 10.0.21 (12/12/2023)

### Changed

- Updated the SDK to compatible with `DynamsoftCaptureVisionRouter` v2.0.21.
- Updated the dependency rules of Dynamsoft SDK modules. Removed transitive dependencies.

## 10.0.20 (10/26/2023)

The first version of `DynamsoftBarcodeReader (DBR)` Android edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.

### New

- Added a new parameter `scaleDownThreshold` to the struct `SimplifiedBarcodeReaderSettings`.

### Fixed

- Small fixes and tweaks.

### Changed

- Removed `BF_PATCH_CODE` from the combined value of `BF_DEFAULT` as decoding Patch Code is not supported by default.
