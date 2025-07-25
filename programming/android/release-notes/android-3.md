---
layout: default-layout
title: Release Notes v3.x - DynamsoftCaptureVisionBundle Android Edition
description:  The release notes of DynamsoftCaptureVisionBundle Android v3.x.
keywords: release notes, capture vision bundle, Android, dcv
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVision Android v3.x

## 3.0.5000 (07/25/2025)

### New

- **Supported 16 KB page sizes**: Updated the `CameraView` class and the `BarcodeScannerActivity` componment to support 16 KB page sizes.

### Changed

- **License Validation Behavior**: Instead of stopping execution immediately on an invalid license module, the library now continues processing and returns results from modules with valid licenses. An error is still reported to indicate the license issue.

### Fixed

- Fixed various minor bugs and improved overall stability.

## 3.0.3100 (05/30/2025)

### Fixed

- Fixed a bug where `CameraEnhancer.open ` might not work when triggered before the finish of the onCreate of the lifecycle.
- Fixed a bug where the click event of the `ArcDrawingItem` might not be triggered when there is a `ScanRegion`.
- Fixed a bug where the `ArcDrawingItem` might be displayed incorrectly when there is a `ScanRegion`.

## 3.0.3000 (05/15/2025)

### [Highlights](https://www.dynamsoft.com/release-highlights/?product=dcv3.0)

- Workflow Improvements
  - Restructured the parameter control hierarchy at all levels for finer scope definition and more granular process management, with the stage level newly added.
  - Enabled custom combinations and sequences of sections, increasing flexibility and operational customization under specific conditions.
  - Redesigned document normalization sections to better accommodate diverse document processing operations.
  
- Deep Learning Integration
  - Improved the reading rate of 1D barcode by introducing a new deblurring deep-learning model.
  - Enhanced text recognition capabilities with deep learning-based text-line recognition.

- Algorithm Enhancements
  - Enabled deduplication at the Region of Interest (ROI) level to consolidate results from multiple tasks.
  - Enhanced the text recognition workflow by integrating improved multi-step recognition processes and validation methods.
  - Improved the CODE_128 and DataMatrix DeepAnalysis algorithms for better decoding accuracy and performance.
  - Added support for new barcode types: CODE_32, MATRIX_25, KIX, and TELEPEN.
  - Added GS1 Application Identifiers (AI) support for improved code parsing capabilities.

- Engineering Optimizations
  - Unified template-loading logic to reduce I/O overhead.
  - Implemented conversion functionality between `ImageData` and image files, including both on-disk and in-memory files.
