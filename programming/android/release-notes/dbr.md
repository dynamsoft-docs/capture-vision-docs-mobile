---
layout: default-layout
title: DBR Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of DynamsoftBarcodeReader module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, barcode reader, Android, DBR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftBarcodeReader Module

## 10.2.10 (04/16/2024)

### New

- Added new methods to the `CandidateBarcodeZonesUnit` class to add, remove or set the candidate barcode zones. `CandidateBarcodeZone` class is added to store the information of a single candidate barcode zone.
- Added new methods to the `LocalizedBarcodesUnit` class to add, remove or set the localized barcode elements.
- Added a new method `setImageData` to the `ScaledUpBarcodeImageUnit` class.
- Added new methods to the `DeformationResistedBarcodeImageUnit` class to add, remove or set the deformation-resisted barcode. `DeformationResistedBarcode` class is added to store the deformation-resisted barcode information.
- Added a new method SetLocation to `ComplementedBarcodeImageUnit` class.
- Added new methods to the `DecodedBarcodesUnit` class to set or remove the decoded barcode elements.
- Added the following methods to the `DecodedBarcodesResult` class:
  - `retain`
  - `release`.
- Added new constructors to the following classes.
  - `DecodedBarcodeElement`
  - `LocalizedBarcodeElement`
- Added the following methods to the `DecodeBarcodeElement` class to modify the basic information of the barcode:
  - `setFormat`
  - `setText`
  - `setBytes`
  - `setConfidence`
- Added a new method `setPossibleFormats` to the `LocalizedBarcodeElement`.

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
