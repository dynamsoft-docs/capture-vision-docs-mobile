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
| [`capturedResultItemTypes`](#capturedresultitemtypes) | *NSInteger* | Specifies the types of result items that are expected to be returned. |
| [`roi`](#roi) | *DSQuadrilateral \** | Designates the region of interest (ROI) within an image, limiting the image processing activities exclusively to this specified area. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *BOOL* | Determines if the coordinates for the region of interest (ROI) are expressed in percentage terms (true) or as exact pixel measurements (false). |
| [`maxParallelTasks`](#maxparalleltasks) | *NSInteger* | Specifies the maximum number of parallel tasks that can be used for image capture and recognition. |
| [`timeout`](#timeout) | *NSInteger* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |
| [`barcodeSettings`](#barcodesettings) | *DSSimplifiedBarcodeReaderSettings \** | Specifies the basic settings for the barcode reader module. |
| [`labelSettings`](#labelsettings) | *DSSimplifiedLabelRecognizerSettings \** | Specifies the basic settings for the label recognizer module. |
| [`documentSettings`](#documentsettings) | *DSSimplifiedDocumentNormalizerSettings \** | Specifies the basic settings for document normalizer module. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *NSInteger* | Set the minimum capture interval. It is measured in millisecond. |

### capturedResultItemTypes

Specifies the types of result items that are expected to be returned.

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

Specifies the basic settings for the barcode reader module.

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

Specifies the basic settings for the label recognizer module.

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

Specifies the basic settings for document normalizer module.

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
