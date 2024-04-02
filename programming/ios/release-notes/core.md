---
layout: default-layout
title: Core Module Release Notes - Dynamsoft Capture Vision iOS Edition
description: The release notes of Dynamsoft Capture Vision iOS Edition.
keywords: release notes, core, iOS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCore Module

## 3.2.10 (03/07/2024)

### New

- Added a new property `resultUnitTypesOnlyForInput` to the `DSObservationParameters` class to specify the `input only` result unit.
- Added the following methods to the `DSRegionObjectElement` class to support the intermediate result modification.
  - `setLocation`
  - `clone`
  - `retain`
  - `release`
- Added a new method `replace` to the `DSIntermediateResultUnit` class to support the replacement of intermediate result units.
- Added `setImageData` methods to the following classes:
  - `DSColourImageUnit`
  - `DSScaledDownColourImageUnit`
  - `DSGrayscaleImageUnit`
  - `DSTransformedGrayscaleImageUnit`
  - `DSEnhancedGrayscaleImageUnit`
  - `DSBinaryImageUnit`
  - `DSTextureRemovedGrayscaleImageUnit`
  - `DSTextureRemovedBinaryImageUnit`
  - `DSTextRemovedBinaryImageUnit`
- Added new methods to the `DSPredetectedRegionsUnit` class to add, remove or set the predetected regions.
- Added new methods to the `DSLineSegmentsUnit` class to add, remove or set the line segments.
- Added new methods to the `DSTextZonesUnit` class to add, remove or set the text zones. Added a new class `TextZone` to store the information of a single text zone.
- Added a new method `setContours` to the `DSContourUnit` class.
- Added new methods to the `DSTextureDetectionResultUnit` class to set the X & Y spacing.
- Added a new intermediate result unit, `DSShortLinesUnit`, to output the detected short lines. The corresponding enumeration member `DSIntermediateResultUnitTypeShortLines` is added to the `DSIntermediateResultUnitType`.
- Added the following methods to the `DSCapturedResultItem` class
  - `getTargetROIDefName`
  - `getTaskName`
  - `retain`
  - `release`
- Added the following new error codes
  - `DSErrorImageSizeNotMatch`
  - `DSErrorImagePixelFormatNotMatch`
  - `DSErrorSectionLevelResultIrreplaceable`
  - `DSErrorAxisDefinitionIncorrect`
  - `DSErrorTextLineGroupLayoutConflict`
  - `DSErrorTextLineGroupRegexConflict`
- Added the following methods to the `DSCapturedResult` class.
  - `retain`
  - `release`
- The following classes are moved to `DSCaptureVisionRouter` module:
  - `DSCapturedResult`
  - `DSIntermediateResultReceiver`
  - `DSCapturedResultReceiver`
  - `DSCapturedResultFilter`
  - `DSIntermediateResultManager`
- Added a new supported image pixel format, binary 8 inverted. The corresponding enumeration member is added to the `DSImagePixelFormat`.
- Added return value for the `retain` method of the `DSIntermediateResultUnit` class. The method will return the pointer of the current `DSIntermediateResultUnit`.

### Breaking Changes

- Refactored the `DSContour` class. Please view API reference - `DSContour` class for more information.

### Fixed

- Fixed a crash bug that might happen when triggering the `setNextImageToReturn` method of the `DSImageSourceAdapter` class.

## 3.0.20 (10/26/2023)

### New

- Added `DSImageSourceErrorListener` to receive the errors from an image source.
- Added method `setErrorListener` to class `DSImageSourceAdapter` to add the `DSImageSourceErrorListener`.
- Added the following error codes:
  - `DSErrorFileAlreadyExists`
  - `DSErrorCreateFileFailed`
  - `DSErrorImageDataInvalid`

### Fixed

- Small fixes and tweaks.

### Changed

- Changed the timing of `onOriginalImageResultReceived` so that it is triggered immediately after receiving the image.

## 3.0.10 (08/10/2023)

The first version of `DynamsoftCore` iOS edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
