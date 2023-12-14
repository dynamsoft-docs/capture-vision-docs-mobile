---
layout: default-layout
title: CVR Module Release Notes - Dynamsoft Capture Vision Android Edition
description:  The release notes of CaptureVisionRouter module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, capture vision router, Android, cvr
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - CaptureVisionRouter Module

## v2.0.20

### New

- Added the following preset templates:
  - PT_READ_BARCODES_SPEED_FIRST;
  - PT_READ_BARCODES_READ_RATE_FIRST;
  - PT_READ_BARCODES_BALANCED;
  - PT_READ_SINGLE_BARCODE;
  - PT_READ_DENSE_BARCODES;
  - PT_READ_DISTANT__BARCODES;
  - PT_RECOGNIZE_NUMBERS;
  - PT_RECOGNIZE_LETTERS;
  - PT_RECOGNIZE_NUMBERS_AND_LETTERS;
  - PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS;
  - PT_RECOGNIZE_UPPERCASE_LETTERS;
- Added parameter `Page` to `ImageSource` object.
- Added a new parameter `minImageCaptureInterval` which can be set via the struct `SimplifiedCaptureVisionSettings` or the `CaptureVisionTemplate` object of a JSON template file.
- Added "UNKNOWN" as a supported value of the `TextDetectionMode.Direction` parameter. Changed the default value of `Direction` to "UNKNOWN".

### Improved

- Optimize the logic to support calling `IntermediateResultManager.addResultReceiver` and  `IntermediateResultManager.removeResultReceiver` after StartCapturing.
- Added ability to output all templates via methods `outputSettings` and `outputSettingsToFile` by specifying "*" for the parameter `templateName`.

### Fixed

- Small fixes and tweaks.
