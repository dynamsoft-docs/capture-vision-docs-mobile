---
layout: default-layout
title: Release Notes v3.x - DynamsoftCaptureVisionBundle Android Edition
description:  The release notes of DynamsoftCaptureVisionBundle Android v3.x.
keywords: release notes, capture vision bundle, Android, dcv
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVision Android v3.x

## 3.6.2000 (08/14/2026)

### New

- Added support for Micro PDF417-specific decoding mode.

### Fixed

- Fixed several known crash issues.

## 3.6.1000 (07/30/2026)

### Highlights

#### Multi-Threaded Barcode Decoding

- **Get results sooner with parallel processing** - Barcode decoding now uses a breadth-first strategy that decomposes a single DBR Task into one Localization Work and one or more Decoding Works. This improves thread utilization and reduces the chance that a slow `DeblurMode` attempt blocks other faster decoding attempts, helping valid results come back sooner.

#### DataMatrix Color Inversion Detection

- **Handle normal and inverted DataMatrix more efficiently** - Added [`AutoDetectColorInversion`]({{ site.dcvb_parameters_reference }}barcode-format-specification/auto-detect-color-inversion.html) to automatically handle both normal and inverted DataMatrix barcodes. Instead of processing the whole image twice, the SDK applies dual-polarity handling only to localized DataMatrix regions, which makes processing faster in dual-polarity scenarios.

#### Barcode Layout Analysis

- **Decode dense grid barcodes more completely** - Added [`LayoutAnalyzer`]({{ site.dcvb_android_api }}utility/layout-analyzer.html) to organize barcode locations into logical line or matrix layouts and infer unrecognized barcode regions when gaps exist, enabling workflows such as fast first-pass decoding, missing-region inference, and targeted second-pass decoding on dense N*M barcode layouts.

#### Cross-Version License Support

- **Use a single license across SDK versions** - Full License 1.0 keys (starting with "f") that are non-perpetual are no longer version-checked, so the same key can be used across SDK versions without reactivation.

#### Text Line Orientation Detection

- **Improved handling of rotated text lines** - Added [`OrientationDetectionModes`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/orientation-detection-modes.html) to detect text line orientation and correct it for further processing. Two modes are available: `ODM_SPATIAL_REFERENCES` and `ODM_CHARS_ORIENTATION_NEURAL_NETWORK`.
- **Current limitations** - This capability is currently effective only in MRZ scenarios and supports only upright and upside-down text lines (0 degrees and 180 degrees). It does not yet handle 90 degrees, 270 degrees, or arbitrary rotation angles.

### New

- Added [`AutoDetectColorInversion`]({{ site.dcvb_parameters_reference }}barcode-format-specification/auto-detect-color-inversion.html) parameter for `BarcodeFormatSpecification` to support automatic color-inversion detection for DataMatrix barcodes.

- Added [`LayoutAnalyzer`]({{ site.dcvb_android_api }}utility/layout-analyzer.html) class with [`analyze()`]({{ site.dcvb_android_api }}utility/layout-analyzer.html#analyze) static method for quadrilateral layout analysis.

- Added [`LayoutPattern`]({{ site.dcvb_android_api }}utility/enum-layout-pattern.html) enumeration with values `LP_UNKNOWN`, `LP_LINES`, and `LP_MATRIX`.

- Added [`LayoutElementSource`]({{ site.dcvb_android_api }}utility/enum-layout-element-source.html) enumeration with values `LES_NONE`, `LES_INPUT`, and `LES_INFERRED`.

- Added [`MeasureUnit`]({{ site.dcvb_android_api }}core/enum-measure-unit.html) enumeration with values `MU_PIXEL` and `MU_PERCENTAGE`.

- Added [`LayoutAxis`]({{ site.dcvb_android_api }}utility/layout-axis.html), [`LayoutAnalysisParameter`]({{ site.dcvb_android_api }}utility/layout-analysis-parameter.html), [`LayoutElement`]({{ site.dcvb_android_api }}utility/layout-element.html), and [`LayoutAnalysisResult`]({{ site.dcvb_android_api }}utility/layout-analysis-result.html) for layout analysis configuration and results.

- Added a new `GridBarcodeScanner` sample (with `sample_grid.png`) to demonstrate how to use [`LayoutAnalyzer`]({{ site.dcvb_android_api }}utility/layout-analyzer.html) for barcode grid layout detection and logical row/column mapping.

- Added [`OrientationDetectionModes`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/orientation-detection-modes.html) parameter for the [`SST_LOCALIZE_TEXT_LINES`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/stage-localize-text-lines.html) stage with two supported modes: `ODM_SPATIAL_REFERENCES` and `ODM_CHARS_ORIENTATION_NEURAL_NETWORK`.

- Added `TextLineOrientationCls.data` model file for text line orientation classification.

### Changed

- [`MaxParallelTasks`]({{ site.dcvb_parameters_reference }}capture-vision-template/max-parallel-tasks.html) now controls the total number of Work-level threads in the CVR thread pool. For DBR tasks, each Localization Work and Decoding Work occupies one thread slot. DLR and DDN tasks continue to occupy one thread per task.

- [`set_device_friendly_name()`]({{ site.dcvb_android_api }}license/license-manager.html#set_device_friendly_name) now enforces parameter constraints: maximum 64 characters, allowed characters are letters (a-z, A-Z), digits (0-9), hyphen (-), underscore (_), and period (.), and must start and end with a letter or digit. Returns [`EC_PARAMETER_VALUE_INVALID`]({{ site.dcvb_android_api }}core/enum-error-code.html) if constraints are not met.

- Improved the default display behavior of corner adjustment points in `ImageEditorView`. Previously, users had to tap the view before the corner adjustment points became visible.

### Fixed

- Fixed an issue in GS1-Databar AI `17` (YYMMDD) results where the month field could be missing a leading zero.

## 3.4.3000 (07/07/2026)

### Security Updates

- Updated third-party libraries to incorporate the latest security fixes.

## 3.4.1300 (05/20/2026)

### Fixed

- Fixed potential issues that could occur on devices running a kernel with a 16KB page size.
- Fixed crash and hang issues that could occur in certain scenarios.

## 3.4.1200 (04/02/2026)

### Improved

- Updated camera lifecycle management code to improve stability.

### Fixed

- Fixed an issue where downloading deep learning models could fail.

## 3.4.1000 (02/05/2026)

### Highlights

#### AI-Powered Barcode Detection and Decoding

- **PDF417 Localization Model** – Introduces the `PDF417Localization` neural network model for improved detection of PDF417 barcodes, especially under challenging conditions.
- **Code39/ITF Decoding Model** – Adds the `Code39ITFDecoder` model for enhanced decoding of Code 39 and ITF barcodes under blurred or low-resolution conditions.
- **Deblur Models for 2D Barcodes** – Adds the `DataMatrixQRCodeDeblur` and `PDF417Deblur` models provide more effective recovery from motion and focus blur for DataMatrix, QR Code, and PDF417 barcodes.

#### ECI (Extended Channel Interpretation) Support

- **ECI Information Return** – Adds support for retrieving Extended Channel Interpretation (ECI) data from barcodes. The new [`ECISegment`]({{ site.dbr_android_api }}eci-segment.html) class, along with [`getECISegments`]({{ site.dbr_android_api }}barcode-result-item.html#getecisegments) method in [`BarcodeResultItem`]({{ site.dbr_android_api }}barcode-result-item.html) class, enables access to character encoding information embedded in barcodes.
- **ECI-Based Text Interpretation** – Adds support for interpreting ECI segments during barcode decoding, improving compatibility with international character sets.

#### Performance Improvements

- **On-Demand Model Loading** – Implements lazy loading for AI models, reducing initialization time by loading models only when first needed.
- **Smart Model Selection** – Models are now loaded based on configured barcode formats, minimizing memory usage by excluding unused models.
- **Improved Confidence Scoring** – Enhances confidence score calculation for results from neural network models, providing more accurate quality indicators.
- **DPM Barcode Optimization** – Improves recognition rate for Direct Part Marking (DPM) barcodes commonly used in industrial and manufacturing environments.

#### Identity Document Processing

- **Enhanced Passport Processing** – Improves document edge detection accuracy for passport documents through optimized processing workflows.
- **Portrait Zone Detection** – The `MRZLocalization` model now supports detecting portrait zone on identity documents, enabling automatic extraction of photo regions.
- **New DynamsoftIdentityUtility Module** – Introduces a dedicated module for identity document processing, including the [`IdentityProcessor`]({{ site.dcv_android_api }}identity-utility/identity-processor.html) class with `findPortraitZone` method for precise portrait positioning from passports and ID cards.

### New

- Added [`BarcodeZoneWidthToHeightRatioRangeArray`]({{ site.dcv_parameters_reference }}barcode-format-specification/barcode-zone-width-to-height-ratio-range-array.html) parameter for filtering barcodes based on aspect ratio constraints.
- Added [`setResultCrossVerificationCriteria`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html#setresultcrossverificationcriteria) and [`getResultCrossVerificationCriteria`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html#getresultcrossverificationcriteria) methods to [`MultiFrameResultCrossFilter`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html) for configurable multi-frame result verification.
- Added [`AuxiliaryRegionElement`]({{ site.dcv_android_api }}core/intermediate-results/auxiliary-region-element.html) class for representing additional region information detected during processing (e.g., MRZ (Machine Readable Zone), portrait zones).
- Added `ROET_AUXILIARY_REGION` to [`RegionObjectElementType`]({{ site.dcv_android_api }}core/enum/region-object-element-type.html) enumeration for the new [`AuxiliaryRegionElement`]({{ site.dcv_android_api }}core/intermediate-results/auxiliary-region-element.html) class.
- Added auxiliary region element management methods to [`LocalizedTextLinesUnit`]({{ site.dlr_android_api }}localized-text-lines-unit.html):
  - `getAuxiliaryRegionElementsCount`
  - `getAuxiliaryRegionElement`
  - `getAuxiliaryRegionElements`
  - `setAuxiliaryRegionElement`
  - `addAuxiliaryRegionElement`
  - `removeAuxiliaryRegionElement`
  - `removeAllAuxiliaryRegionElements`
- Added new error code `EC_PORTRAIT_ZONE_NOT_FOUND` for identity document processing.
- Added a new resolution [`RESOLUTION_MAX`]({{ site.dce_android_api }}enum/resolution.html) for capturing photos at maximum resolution (3024*4032).
- Added a new listener [`FocusListener`]({{ site.dce_android_api }}auxiliary-api/interface-focus-listener.html) for receiving callback when the camera focus is completed. You can register the listener via [`CameraEnhancer.setFocusListener`]({{ site.dce_android_api }}primary-api/camera-enhancer.html#setfocuslistener).

### Changed

- Barcode text encoding fallback changed from UTF-8 to ISO-8859-1 when no ECI information is present in the barcode.
- Improved license binding stability on MacOS devices.
- Updated default value of `compensation` parameter in [`ImageProcessor.convertToBinaryLocal`]({{ site.dcv_android_api }}utility/image-processor.html#converttobinarylocal) from 0 to 10.
- [`convertToBinaryGlobal`]({{ site.dcv_android_api }}utility/image-processor.html#converttobinaryglobal) and [`convertToBinaryLocal`]({{ site.dcv_android_api }}utility/image-processor.html#converttobinarylocal) of `ImageProcessor` class now support color and binary images as input in addition to grayscale images.

### Removed

- Removed `DataMatrixModuleIsotropic` parameter – use [`BarcodeZoneWidthToHeightRatioRangeArray`]({{ site.dcv_parameters_reference }}barcode-format-specification/barcode-zone-width-to-height-ratio-range-array.html) instead.
- Removed `MinRatioOfBarcodeZoneWidthToHeight` parameter – use [`BarcodeZoneWidthToHeightRatioRangeArray`]({{ site.dcv_parameters_reference }}barcode-format-specification/barcode-zone-width-to-height-ratio-range-array.html) instead.

### Fixed

- Fixed incorrect coordinate in barcode result when using neural network models with a specified region.
- Fixed crash and hang issues that could occur in certain scenarios.
- Fixed various minor bugs and improved overall stability.

## 3.2.5000 (12/16/2025)

This release includes security maintenance updates to ensure continued protection of the product.

### Security Updates

- Updated third-party libraries to incorporate the latest security fixes.

## 3.2.3000 (11/05/2025)

### Fixed

- Resolved an issue where `CaptureVisionRouter.startCapturing` could take longer than expected to complete.
- Fixed an issue where `initLicense` could take longer than expected to complete.
- Fixed an issue where the app could crash when a `CameraView` instance was created using `new CameraView()`.
- Fixed a potential crash that could occur in certain scenarios.

## 3.2.1000 (10/16/2025)

### 🎉Milestone Release

Version 3.2.1000 introduces a series of AI-driven improvements designed to enhance barcode and MRZ detection accuracy, processing speed, and configuration flexibility.

This release focuses on practical performance gains for production environments across retail, logistics, manufacturing, and identity verification workflows.

### ✨ Key Highlights

#### AI-Powered Barcode Detection and Decoding

- New Localization Models – Introduces [`OneDLocalization`]({{ site.dcv_parameters_reference }}barcode-reader-task-settings/localization-modes.html#modelnamearray) and [`DataMatrixQRCodeLocalization`]({{ site.dcv_parameters_reference }}barcode-reader-task-settings/localization-modes.html#modelnamearray) neural network models for improved detection of **blurred / low-resolution 1D codes**, or **partially damaged DataMatrix/QR codes**.
- Specialized Decoders – Adds [`EAN13Decoder`]({{ site.dcv_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) and [`Code128Decoder`]({{ site.dcv_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) models optimized for **long-distance** and **motion-blurred** decoding scenarios.
- Redesigned Deblur Model – The [`OneDDeblur`]({{ site.dcv_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#modelnamearray) model now provides more effective recovery from **motion and focus blur**.
- Configurable Model Selection – The new `ModelNameArray` parameter supports flexible model loading and fine-grained control for specific barcode types.

#### Precision and Processing Control

- Enhanced Deblur Methods – [`DM_DEEP_ANALYSIS`]({{ site.dcv_parameters_reference }}barcode-reader-task-settings/deblur-modes.html#dm_deep_analysis) now includes sub-level control with `OneDGeneral`, `TwoDGeneral`, and `EAN13Enhanced` options.
- Barcode Count Expectation – The new [`ExpectedBarcodesCount`]({{ site.dcv_parameters_reference }}barcode-format-specification/expected-barcodes-count.html) parameter enables **format-specific quantity control** and **early termination** in fixed-count workflows.
- Improved Region Detection – The new [`RPM_GRAY_CONSISTENCY`]({{ site.dcv_parameters_reference }}image-parameter/region-predetection-modes.html#rpm_gray_consistency) mode provides more precise region extraction based on **grayscale uniformity** and **local consistency** for document and label processing.

#### AI-Powered MRZ Detection

- Neural MRZ Localization – The new [`MRZLocalization`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/localization-modes.html#modelnamearray) model improves region detection accuracy and delivers up to **42.7%** faster processing for MRZ-based document workflows.
- Configurable Localization Control – The new [`LocalizationModes`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/localization-modes.html) parameter allows configuration for text line detection.

#### Smart Document Capture

- Clarity-Based Frame Selection – Automatically selects the sharpest and highest-quality frame in live capture workflows.
- Cross-Frame Verification – Updated verification algorithms enhance result reliability.

### Performance Highlights

#### Barcode Workflows

- Up to **26.5%** higher read rates under blur conditions with as much as **44%** faster processing.
- Reliable decoding of DataMatrix and QR codes with missing or damaged finder patterns.
- Extended operational range beyond 75 cm for long-distance barcode scanning.

#### Document Workflows

- Improved performance in live video capture environments.
- Consistent document quality through clarity-based frame evaluation.
- Faster MRZ processing for high-throughput identity verification

### Developer Notes

- Backward Compatibility – Fully compatible with existing integrations; no code-level changes required for upgrade.
- Configuration Flexibility – Expanded parameter set allows comprehensive model configuration for scenario-specific tuning.
- Production Stability – All new models validated in enterprise environments.

### New

- Added a new method, [`switchCapturingTemplate`]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#switchcapturingtemplate), which allows switching templates dynamically during the image processing workflow.
- Added a new method, [`clearDLModelBuffers`]({{ site.dcv_android_api }}capture-vision-router/settings.html#cleardlmodelbuffers), to release memory by clearing buffered deep learning models.
- Added a new method, [`setGlobalIntraOpNumThreads`]({{ site.dcv_android_api }}capture-vision-router/settings.html#setglobalintraopnumthreads), to configure the global number of threads used for model execution.
- Added a new button, `cameraToggleButton`, to the `CameraView`, allowing users to switch between the front and back cameras.
The following APIs are provided for configuring the `cameraToggleButton`:
  - [`setCameraToggleButton`]({{ site.dce_android_api }}auxiliary-api/dcecameraview.html#setcameratogglebutton)
  - [`setCameraToggleButtonVisible`]({{ site.dce_android_api }}auxiliary-api/dcecameraview.html#setcameratogglebuttonvisible)
  - [`getCameraToggleButtonVisible`]({{ site.dce_android_api }}auxiliary-api/dcecameraview.html#getcameratogglebuttonvisible)

### Changed

- Changed the enumeration value of [`EnumEnhancerFeatures`]({{ site.dce_android_api }}enum/enhanced-features.html):
  - Changed `EF_AUTO_ZOOM` from `1 << 4` to `1 << 3`.
  - Changed `EF_SMART_TORCH` from `1 << 5` to `1 << 4`.
  - Changed `EF_ALL` from `0x3F` to `0x1F`.

## 3.0.5000 (07/29/2025)

### New

- **Supported 16 KB page sizes**.

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
