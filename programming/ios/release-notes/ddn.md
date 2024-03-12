---
layout: default-layout
title: DDN Module Release Notes - Dynamsoft Capture Vision iOS Edition
description: The release notes of DynamsoftDocumentNormalizer module - Dynamsoft Capture Vision iOS Edition.
keywords: release notes, document normalizer, iOS, DDN
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftDocumentNormalizer Module

## 2.2.10 (03/07/2024)

### New

- Added new methods to the `DSLongLinesUnit` class to add, set or remove the line segments of the unit.
- Added new methods to the `DSCornersUnit` class to add, set or remove the corners of the unit.
- Added new methods to the `DSCandidateQuadEdgesUnit` class to add, set or remove the candidate quad edges of the unit.
- Added new methods to the `DSDetectedQuadsUnit` class to add, set or remove the detected quad elements of the unit.
- Added new methods to the `DSNormalizedImagesUnit` class to set or remove the normalized image element of the unit.
- Added the following methods to the `DSNormalizedImagesResult` class.
  - `retain`
  - `release`
- Added the following methods to the `DSDetectedQuadsResult` class.
  - `retain`
  - `release`
- Added `DSSimplifiedDocumentNormalizerSettings` class to configure basic settings of document processing.
- Added new constructors to the following classes.
  - `DSNormalizedImageElement`
  - `DSDetectedQuadElement`
- Added a new enumeration `DSImageColourMode` to specify the colour mode of the normalized image.

### Fixed

- Fixed a bug where the internal table boundaries were recognized as the document boundaries.

## 2.0.20 (12/12/2023)

### Changed

- Updated the SDK to compatible with `DynamsoftCaptureVisionRouter` v2.0.21.
- Updated the dependency rules of Dynamsoft SDK modules. Removed transitive dependencies.

### Fixed

- Small fixes and tweaks.

## 2.0.10 (08/10/2023)

The first version of `DynamsoftDocumentNormalizer (DDN)` iOS edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
