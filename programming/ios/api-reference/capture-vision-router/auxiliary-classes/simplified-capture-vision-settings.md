---
layout: default-layout
title: DSSimplifiedCaptureVisionSettings - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSSimplifiedCaptureVisionSettings of Dynamsoft Capture Vision Router Module contains settings for capturing and recognizing images with the DSCaptureVisionRouter class.
keywords: Capture Vision settings, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSSimplifiedCaptureVisionSettings

The `DSSimplifiedCaptureVisionSettings` class contains settings for capturing and recognizing images with the `DSCaptureVisionRouter` class.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSSimplifiedCaptureVisionSettings : NSObject
```
2. 
```swift
class SimplifiedCaptureVisionSettings : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`capturedResultItemTypes`](#capturedresultitemtypes) | *NSInteger* | Specifies the type(s) of CapturedItem(s) that will be captured. |
| [`roi`](#roi) | *DSQuadrilateral \** | Specifies the region of interest (ROI) where the image capture and recognition will take place. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *BOOL* | Specifies whether the ROI is measured in pixels or as a percentage of the image size. |
| [`maxParallelTasks`](#maxparalleltasks) | *NSInteger* | Specifies the maximum number of parallel tasks that can be used for image capture and recognition. |
| [`timeout`](#timeout) | *NSInteger* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |
| [`barcodeSettings`](#barcodesettings) | *DSSimplifiedBarcodeReaderSettings \** | Specifies the settings for `DynamsoftBarcodeReader` tasks. |
| [`labelSettings`](#labelsettings) | *DSSimplifiedLabelRecognizerSettings \** | Specifies the settings for `DynamsoftLabelRecognizer` tasks. |
| [`documentSettings`](#documentsettings) | *DSSimplifiedDocumentNormalizerSettings \** | Specifies the settings for `DynamsoftDocumentNormalizer` tasks. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *NSInteger* | Set the minimum capture interval. It is measured in millisecond. |

### capturedResultItemTypes

Specifies the type(s) of CapturedItem(s) that will be captured.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger capturedResultItemTypes;
```
2. 
```swift
var capturedResultItemTypes: Int { get set }
```

### roi

Specifies the region of interest (ROI) where the image capture and recognition will take place.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSQuadrilateral *roi;
```
2. 
```swift
var roi: DSQuadrilateral? { get set }
```

### roiMeasuredInPercentage

Specifies whether the ROI is measured in pixels or as a percentage of the image size.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) BOOL roiMeasuredInPercentage;
```
2. 
```swift
var roiMeasuredInPercentage: Bool { get set }
```

### maxParallelTasks

Specifies the maximum number of parallel tasks that can be used for image capture and recognition.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger maxParallelTasks;
```
2. 
```swift
var maxParallelTasks: Int { get set }
```

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger timeout;
```
2. 
```swift
var timeout: Int { get set }
```

### barcodeSettings

Specifies the settings for `DynamsoftBarcodeReader` tasks with a [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_ios_api }}simplified-barcode-reader-settings.html) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSSimplifiedBarcodeReaderSettings *barcodeSettings;
```
2. 
```swift
var barcodeSettings: DSSimplifiedBarcodeReaderSettings? { get set }
```

### labelSettings

Specifies the settings for `DynamsoftLabelRecognizer` tasks with a [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSSimplifiedLabelRecognizerSettings *labelSettings;
```
2. 
```swift
var labelSettings: DSSimplifiedLabelRecognizerSettings? { get set }
```

### documentSettings

Specifies the settings for `DynamsoftDocumentNormalizer` tasks with a [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_ios_api }}simplified-document-normalizer-settings.html) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSSimplifiedDocumentNormalizerSettings *documentSettings;
```
2. 
```swift
var documentSettings: DSSimplifiedDocumentNormalizerSettings? { get set }
```

### minImageCaptureInterval

Specifies the minimum image capture interval.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger minImageCaptureInterval;
```
2. 
```swift
var minImageCaptureInterval: Int { get set }
```
