---
layout: default-layout
title: DDN Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of DynamsoftDocumentNormalizer module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, document normalizer, Android, DDN
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftDocumentNormalizer Module

## 2.2.11 (05/15/2024)

- Added new methods `toJson` & `fromJson` to `SimplifiedDocumentNormalizerSettings` class.

## 2.2.10 (03/07/2024)

### New

- Added new methods to the `LongLinesUnit` class to add, set or remove the line segments of the unit.
- Added new methods to the `CornersUnit` class to add, set or remove the corners of the unit.
- Added new methods to the `CandidateQuadEdgesUnit` class to add, set or remove the candidate quad edges of the unit.
- Added new methods to the `DetectedQuadsUnit` class to add, set or remove the detected quad elements of the unit.
- Added new methods to the `NormalizedImagesUnit` class to set or remove the normalized image element of the unit.
- Added the following methods to the `NormalizedImagesResult` class.
  - `retain`
  - `release`
- Added the following methods to the `DetectedQuadsResult` class.
  - `retain`
  - `release`
- Added `SimplifiedDocumentNormalizerSettings` class to configure basic settings of document processing.
- Added new constructors to the following classes.
  - `NormalizedImageElement`
  - `DetectedQuadElement`
- Added a new enumeration `EnumImageColourMode` to specify the colour mode of the normalized image.

### Fixed

- Fixed a bug where the internal table boundaries were recognized as the document boundaries.

## 2.0.20 (12/12/2023)

### Changed

- Updated the SDK to compatible with `DynamsoftCaptureVisionRouter` v2.0.21.
- Updated the dependency rules of Dynamsoft SDK modules. Removed transitive dependencies.

### Fixed

- Small fixes and tweaks.

## 2.0.10 (08/10/2023)

The first version of `DynamsoftDocumentNormalizer (DDN)` Android edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
