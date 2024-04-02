---
layout: default-layout
title: Core Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of Dynamsoft Capture Vision Android Edition.
keywords: release notes, core, Android
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCore Module

## 3.2.10 (03/07/2024)

### New

- Added the following methods to the `ObservationParameters` class to specify the `input only` result unit.
  - `setResultUnitTypesOnlyForInput`
  - `getResultUnitTypesOnlyForInput`
- Added the following methods to the `RegionObjectElement` class to support the intermediate result modification.
  - `setLocation`
  - `clone`
  - `retain`
  - `release`
- Added a new method `replace` to the `IntermediateResultUnit` class to support the replacement of intermediate result units.
- Added `setImageData` methods to the following classes:
  - `ColourImageUnit`
  - `ScaledDownColourImageUnit`
  - `GrayscaleImageUnit`
  - `TransformedGrayscaleImageUnit`
  - `EnhancedGrayscaleImageUnit`
  - `BinaryImageUnit`
  - `TextureRemovedGrayscaleImageUnit`
  - `TextureRemovedBinaryImageUnit`
  - `TextRemovedBinaryImageUnit`
- Added new methods to the `PredetectedRegionsUnit` class to add, remove or set the predetected regions.
- Added new methods to the `LineSegmentsUnit` class to add, remove or set the line segments.
- Added new methods to the `TextZonesUnit` class to add, remove or set the text zones. Added a new class `TextZone` to store the information of a single text zone.
- Added a new method `setContours` to the `ContourUnit` class.
- Added new methods to the `TextureDetectionResultUnit` class to set the X & Y spacing.
- Added a new intermediate result unit, `ShortLinesUnit`, to output the detected short lines. The corresponding enumeration member `IRUT_SHORT_LINES` is added to the `EnumIntermediateResultUnitType`.
- Added the following methods to the `CapturedResultItem` class
  - `getTargetROIDefName`
  - `getTaskName`
  - `retain`
  - `release`
- Added the following new error codes
  - `EC_IMAGE_SIZE_NOT_MATCH`
  - `EC_IMAGE_PIXEL_FORMAT_NOT_MATCH`
  - `EC_SECTION_LEVEL_RESULT_IRREPLACEABLE`
  - `EC_AXIS_DEFINITION_INCORRECT`
  - `EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT`
  - `EC_TEXT_LINE_GROUP_REGEX_CONFLICT`
- Added the following methods to the `CapturedResult` class.
  - A new override constructor.
  - `retain`
  - `release`
- The following classes are moved to `CaptureVisionRouter` module:
  - `CapturedResult`
  - `IntermediateResultReceiver`
  - `CapturedResultReceiver`
  - `CapturedResultFilter`
  - `IntermediateResultManager`
- Added a new supported image pixel format, binary 8 inverted. The corresponding enumeration member is added to the `EnumImagePixelFormat`.
- Added return value for the `retain` method of the `IntermediateResultUnit` class. The method will return the pointer of the current `IntermediateResultUnit`.

### Breaking Changes

- Refactored the `Contour` class. Please view API reference - `Contour` class for more information.

### Fixed

- Fixed a crash bug that might happen when triggering the `setNextImageToReturn` method of the `ImageSourceAdapter` class.

## 3.0.20 (10/26/2023)

### New

- Added `ImageSourceErrorListener` to receive the errors from an image source.
- Added method `setErrorListener` to class `ImageSourceAdapter` to add the `ImageSourceErrorListener`.
- Added the following error codes:
  - EC_FILE_ALREADY_EXISTS
  - EC_CREATE_FILE_FAILED
  - EC_IMGAE_DATA_INVALID

### Fixed

- Small fixes and tweaks.

### Changed

- Changed the timing of `onOriginalImageResultReceived` so that it is triggered immediately after receiving the image.

## 3.0.10 (08/10/2023)

The first version of `DynamsoftCore` Android edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
