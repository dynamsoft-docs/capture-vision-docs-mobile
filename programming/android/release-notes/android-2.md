---
layout: default-layout
title: Release Notes - DynamsoftCaptureVisionBundle Android Edition
description:  The release notes of DynamsoftCaptureVisionBundle Android Edition.
keywords: release notes, capture vision bundle, Android, dcv
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVisionBundle

## 2.4.2000 (10/11/2024)

### Highlights

- Improved the read rate and the speed of the following barcode formats:
  - EAN13
  - DotCode
- Added support for decoding add-on codes (also known as Extension Codes) for UPC-A, UPC-E, EAN-8 and EAN-13 codes.
- Added "Recognize Raw TextLines" stage for recognizing raw text lines.
- Introduced a feature to track and accumulate recognized barcodes across multiple frames in real-time video, enabling seamless multi-barcode recognition.

### DynamsoftCaptureVisionRouter

#### Improved

- Updated the error handling logic of `capturing` & `startCapturing` methods. The methods will be able to clearly report where the error occurred if the capturing fails due to a licensing issue.

#### New

- Added internal logics for usage count.
- Added a new callback method [`onRawTextLinesReceived`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html#onrawtextlinesreceived) to the class `IntermediateResultReceiver`.

### DynamsoftCore

#### New

- Added new error codes
  - -10076: The license is initialized successfully but detected invalid content in your key.
  - -30063: [Barcode Reader] No license found.
  - -40103: [Label Recognizer] No license found.
  - -50058: [Document Normalizer] No license found.
  - -90012: [Code Parser] No license found.
- Added a new enumeration member `IRUT_RAW_TEXT_LINES` to the enumeration [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=android).

#### Fixed

- Fixed a bug where the `CharacterModel` is not correctly loaded under macOS operation system.
- Small fixes and tweaks.

### DynamsoftLicense

#### Improved

- Updated the error message of `initLicense` method. The method will return more detailed messages when failed to initialize the license. Warnings will be available if license initialization is successful but a part of the license key is invalid.

#### New

- Add a new charge way, `TimeSliceCount`.

#### Fixed

- Changed the maximum length of the `deviceFriendlyName` to 255.

### DynamsoftImageProcessing

#### Fixed

- Fixed a crash bug caused by the usage of RegEx.
- Small fixes and tweaks.

#### Changed

- Changed the template loading mode. The library will read all template files under the Templates folder where the DLL file is located.

### DynamsoftUtility

#### New

- Added to-the-latest overlapping feature. You can use [`enableLatestOverlapping`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html#enablelatestoverlapping) method of `MultiFrameResultCrossFilter` class to enable this feature.
- Added a new class [`ProactiveImageSourceAdapter`]({{ site.dcv_android_api }}utility/proactive-image-source-adapter.html). The class [`DirectoryFetcher`]({{ site.dcv_android_api }}utility/directory-fetcher.html) will extends the class `ProactiveImageSourceAdapter` instead of the class `ImageSourceAdapter`.

#### Fixed

- Fixed a bug where `CaptureVisionRouter.startCapturing` would erroneously halt the fetching process when its status was running, leading to an unnecessary stop and restart of the fetching operation.
- Fixed a bug where `DirectoryFetcher` would prematurely read an image before verifying if the buffer was full, resulting in potential loss of the image that did not make it into the buffer upon calling `stopFetching`.

### DynamsoftBarcodeReader

#### Improved

- Improved the read rate and the speed of the following barcode formats:
  - EAN13
  - DotCode

#### New

- Added internal logics for usage count.
- Added support for decoding add-on barcodes.
- Added new properties to the [`QRCodeDetails`]({{ site.dbr_android_api }}auxiliary-QRCodeDetails.html) class
  - `getDataMaskPattern`
  - `getCodewords`

#### Changed

- Updated the Enumeration number of `EnumBarcodeFormat.BF_ALL` to 0xFFFFFFFEFFFFFFFF.
- Updated the internal logic of licensing error message reporting.

#### Fixed

- Fixed a bug that might cause `GS1_DATABAR_EXPANDED_STACKED` barcode unread.

### DynamsoftLabelRecognizer

#### New

- Added internal logics for usage count.
- Added a new parameter [CharSet]({{ site.dcv_parameters_reference }}character-model/char-set.html) to the `CharacterModel` object to include or exclude characters for recognition.
- Added a new algorithm stage `IRUT_RAW_TEXT_LINES`.  Corresponding APIs are added to obtain the intermediate result of this stage.
  - Class [`RawTextLinesUnit`]({{ site.dlr_android_api }}raw-text-lines-unit.html)
  - Class [`RawTextLine`]({{ site.dlr_android_api }}raw-text-line.html)
  - Enumeration [`RawTextLineStatus`]({{ site.dcv_enumerations }}label-recognizer/raw-text-line-status.html?lang=android)
- Changed the intermediate result altering methods of the class [`RecognizedTextLinesUnit`]({{ site.dlr_android_api }}recognized-text-lines-unit.html).
  - Added method `removeRecognizedTextLine`
  - Added method `addRecognizedTextLine`
  - Added method `setRecognizedTextLine(index,element,matrixToOriginalImage)`
  - Deprecated method `setRecognizedTextLine(element,matrixToOriginalImage)`
- Added a new method `getRawText` to the class [`RecognizedTextLineELement`]({{ site.dlr_android_api }}recognized-text-line-element.html).
- Added a new method `getRawText` to the class [`TextLineResultItem`]({{ site.dlr_android_api }}text-line-result-item.html).

#### Fixed

- Fixed a bug where the `CharacterModel` is not correctly loaded under macOS operation system.
- Fixed a crash bug caused by the usage of RegEx.

### DynamsoftNocumentNormalizer

#### New

- Added a new parameter `MinDocumentAreaRatio` to define the minimum targeting document area. The parameter is available via both the parameter template and the [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_android_api }}simplified-document-normalizer-settings.html).
- Added a new parameter `ExpectedDocumentsCount` to define the expected document count for detection. The parameter is available via both the parameter template and the [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_android_api }}simplified-document-normalizer-settings.html).

#### Changes

- Updated internal logics to to use the latest version of `DynamsoftCore` module.

#### Fixed

- Small fixes and tweaks.

### DynamsoftCodeParser

#### Changed

- Updated the internal logic of licensing error message reporting.

### DynamsoftCodeParserDedicator

#### Fixed

- Fixed a bug where the South African Driver's license might be parsed incorrectly.

## 2.2.3000 (08/21/2024)

### Highlights

- Added confusable character distinguishing: this feature enhances the library’s ability to distinguish between common confusable character sets including {0, o, O}, {1, I, l}, and {5, s, S}, across popular fonts like Arial, Times New Roman, and Verdana, etc.
- Supported confusable character set customization: leveraging the new caching mechanism in the `CaptureVisionRouter (CVR)` module, the library now enables users to customize confusable character sets to meet the needs of specific scenarios.
- Introduced the capability for users to influence the image processing process by altering intermediate results. Users can now clone, edit, and substitute intermediate result units within the callback method of each type. Subsequent operations will then proceed based on the updated unit.
- Introduced a feature for multi-condition filtering across products. Users can now specify filtering criteria for the task results of a [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) by implementing an OutputTaskSetting based on the task results of varying products from descendant `TargetROIDef` objects.
- Enhanced the [`Offset`]({{ site.dcv_parameters_reference }}target-roi-def/location.html#offset) parameter in `TargetROIDef`. Users now have the capability to meticulously customize components of the coordinate system, including the origin, X-axis, and Y-axis, for precise offset calculation.
- Introduced a feature for grouping text lines. A text line group consists of spatially adjacent lines of text. Through the [`TextLineSpecification`]({{ site.dcv_parameters_reference }}text-line-specification/) parameters, users can now do two things:
  - Put text lines in groups and also define the spatial relationship between different groups;
  - Specify whether to concatenate text line results within a group, how to do the concatenation and whether to output the concatenated result.

### DynamsoftCaptureVisionRouter

#### New

- Added a new class [`BufferedItemsManager`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/buffered-items-manager.html) to manage the buffered character items.
- Added a new method [`getBufferedItemsManager`]({{ site.dcv_android_api }}capture-vision-router/buffered-items.html#getbuffereditemsmanager) to get an object of `BufferedItemsManager`.

#### Fixed

- Fixed a bug where the `DynamsoftNeuralNetwork` module failed to load due to a path error.

### DynamsoftCore

- Small fixes and tweaks.

### DynamsoftBarcodeReader

- Added new methods `toJson` & `fromJson` to `SimplifiedBarcodeReaderSettings` class.

### DynamsoftCameraEnhancer

- Added a new constructor of class [`CameraEnhancer`]({{ site.android-api }}camera-enhancer.html).
- Updated the enumeration value of [`EnumCameraPosition`]({{ site.dce-enums }}camera-position.html?lang=android).

### DynamsoftCodeParser

#### Improved

- Security update for `DynamsoftCodeParser` library.

#### Fixed

- Small fixes and tweaks.

### DynamsoftCodeParserDedicator

#### Improved

- Security update for `DynamsoftCodeParserDedicator` library.

#### Fixed

- Small fixes and tweaks.

### DynamsoftImageProcessing

- Fixed a bug where users would not receive proper error messages when attempting to configure `SimplifiedLabelRecognizerSettings` with an incorrect `CharacterModel`.

### DynamsoftLabelRecognizer

#### Improved

- Improved the speed of `TextLineGroup` detection by optimizing internal logic.
- Security update for `DynamsoftLabelRecognizer` library and other corresponding libraries.
- Supported the filter configuration of the characters that are not recognized by the Deep Neural Network via the Filter.txt file.
- Improved the `CharacterModel` loading mechanism. If a model file is available under the assets folder, the `CharacterModel` will be loaded autometically. Otherwise, it will be downloaded from the server.

#### New

- Added a new class [`BufferedCharacterItemSet`]({{ site.dlr_android_api }}buffered-character-item-set.html) to represent a collection of buffered character items and cluster information.
- Added a new class [`BufferedCharacterItem`]({{ site.dlr_android_api }}buffered-character-item.html) to represent a basic item of the buffered characters with its image and features information.
- Added a new class [`CharacterCluster`]({{ site.dlr_android_api }}character-cluster.html) to represent a character cluster generated from the collected buffered character items.
- Added a new method [`getSpecificationName`]({{ site.dlr_android_api }}text-line-result-item.html#getspecificationname) to the `TextLineResultItem` class to get the name of the [`TextLineSpecificationObject`]({{ site.dcv_parameter }}file/auxiliary/textline-specification.html) that generated this `TextLineResultItem`.
- Added a new method [`getSpecificationName`]({{ site.dlr_android_api }}recognized-text-line-element.html#getspecificationname) to the `RecognizedTextLineElement` class to get the name of the [`TextLineSpecificationObject`]({{ site.dcv_parameter }}file/auxiliary/textline-specification.html) that generated this `RecognizedTextLineElement`.
- Added new methods to the [`LocalizedTextLinesUnit`]({{ site.dlr_android_api }}localized-text-lines-unit.html) class to add, set or remove the localized text line elements.
- Added new methods to the [`RecognizedTextLinesUnit`]({{ site.dlr_android_api }}recognized-text-lines-unit.html) class to add, set or remove the recognized text line elements.
- Added a new method `setText` to the [`RecognizedTextLineElement`]({{ site.dlr_android_api }}recognized-text-line-element.html) class.
- Added the following methods to the [`RecognizedTextLinesResult`]({{ site.dlr_android_api }}recognized-text-lines-result.html) class.
  - `retain`
  - `release`
- Added new constructors to the following classes.
  - [`RecognizedTextLineElement`]({{ site.dlr_android_api }}recognized-text-line-element.html)
  - [`LocalizedTextLineElement`]({{ site.dlr_android_api }}localized-text-line-element.html)
- Updated the template system
  - Added new [`LabelRecognizerTaskSettings`]({{ site.dcv_parameter }}reference/label-recognizer-task-settings/) parameters.
    - Added `ConfusableCharactersPath` to define the path of the resource files that store the confusable characters' information.
    - Added `ClusterSamplesCountThreshold` to specify the lowest required sample count for clustering.
  - Added new [`TextLineSpecification`]({{ site.dcv_parameter }}reference/text-line-specification/) parameters.
    - Added `ConfusableCharactersCorrection` to define which confusable characters you are going to distinguish. You can also specify the font type of the characters.
    - Added `ExpectedGroupCount` to define the count of `TextLineGroups` that might exist on the image.

### DynamsoftNeuralNetwork

- Separated from the `DynamsoftImageProcessing` module.

### DynamsoftLicense

#### Improved

- Improved the usage count logic of the concurrent license mode.
- Improved the experience of local cache usage when failing to connect the license server. The renewal of the local cache is optimized as well.

### DynamsoftUtility

#### Fixed

- Small fixes and tweaks.
