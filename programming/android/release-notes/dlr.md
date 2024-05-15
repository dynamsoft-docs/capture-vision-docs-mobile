---
layout: default-layout
title: DLR Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of DynamsoftLabelRecognizer module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, label recognizer, Android, DLR
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftLabelRecognizer Module

## 2.2.30 (05/15/2024)

### Improved

- Improved the speed of `TextLineGroup` detection by optimizing internal logic.
- Security update for `DynamsoftLabelRecognizer` library and other corresponding libraries.
- Supported the filter configuration of the characters that are not recognized by the Deep Neural Network via the Filter.txt file.
- Improved the `CharacterModel` loading mechanism. If a model file is available under the assets folder, the `CharacterModel` will be loaded autometically. Otherwise, it will be downloaded from the server.

### New

- Added a new class [`BufferedCharacterItemSet`]({{ site.dlr_android_api }}buffered-character-item-set.html) to represent a collection of buffered character items and cluster information.
- Added a new class [`BufferedCharacterItem`]({{ site.dlr_android_api }}buffered-character-item.html) to represent a basic item of the buffered characters with its image and features information.
- Added a new class [`CharacterCluster`]({{ site.dlr_android_api }}character-cluster.html) to represent a character cluster generated from the collected buffered character items.
- Added a new method [`getSpecificationName`]({{ site.dlr_android_api }}text-line-result-item.html#getspecificationname) to the `TextLineResultItem` class to get the name of the [`TextLineSpecificationObject`]({{ site.dcv_parameter }}file/auxiliary/textline-specification.html){:target="_blank"} that generated this `TextLineResultItem`.
- Added a new method [`getSpecificationName`]({{ site.dlr_android_api }}recognized-text-line-element.html#getspecificationname) to the `RecognizedTextLineElement` class to get the name of the [`TextLineSpecificationObject`]({{ site.dcv_parameter }}file/auxiliary/textline-specification.html){:target="_blank"} that generated this `RecognizedTextLineElement`.
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
  - Added new [`LabelRecognizerTaskSettings`]({{ site.dcv_parameter }}reference/label-recognizer-task-settings/){:target="_blank"} parameters.
    - Added `ConfusableCharactersPath` to define the path of the resource files that store the confusable characters' information.
    - Added `ClusterSamplesCountThreshold` to specify the lowest required sample count for clustering.
  - Added new [`TextLineSpecification`]({{ site.dcv_parameter }}reference/text-line-specification/){:target="_blank"} parameters.
    - Added `ConfusableCharactersCorrection` to define which confusable characters you are going to distinguish. You can also specify the font type of the characters.
    - Added `ExpectedGroupCount` to define the count of `TextLineGroups` that might exist on the image.


<!-- 
## 3.2.0 (03/07/2024)

### New

- Added new methods to the `LocalizedTextLinesUnit` class to add, set or remove the localized text line elements.
- Added new methods to the `RecognizedTextLinesUnit` class to add, set or remove the recognized text line elements.
- Added a new method `setText` to the `RecognizedTextLineElement` class.
- Added the following methods to the `RecognizedTextLinesResult` class.
  - `retain`
  - `release`
- Added new constructors to the following classes.
  - `RecognizedTextLineElement`
  - `LocalizedTextLineElement` -->

## 2.0.20 (12/07/2023)

The first version of `DynamsoftLabelRecognizer (DLR)` Android edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
