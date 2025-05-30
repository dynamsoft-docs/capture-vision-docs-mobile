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

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`outputOriginalImage`](#outputoriginalimage) | *BOOL* | Specifies whether to return the original image in the captured results. |
| [`roi`](#roi) | *[DSQuadrilateral](../../core/basic-structures/quadrilateral.md)* | Specifies the region of interest (ROI) of the image or frame where the capture and recognition will take place. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *BOOL* | Specifies whether the ROI is measured in pixels (false) or as a percentage of the image dimensions (true). |
| [`maxParallelTasks`](#maxparalleltasks) | *NSInteger* | Specifies the maximum number of parallel tasks that can be used for image capture and recognition. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *NSInteger* | Set the minimum capture interval, measured in milliseconds. |
| [`timeout`](#timeout) | *NSInteger* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |
| [`barcodeSettings`](#barcodesettings) | *[DSSimplifiedBarcodeReaderSettings]({{ site.dbr_ios_api }}simplified-barcode-reader-settings.html)* | Specifies the settings for the `DynamsoftBarcodeReader` task. |
| [`labelSettings`](#labelsettings) | *[DSSimplifiedLabelRecognizerSettings]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html)* | Specifies the settings for the  `DynamsoftLabelRecognizer` task. |
| [`documentSettings`](#documentsettings) | *[SimplifiedDocumentNormalizerSettings]({{ site.ddn_ios_api }}simplified-document-normalizer-settings.html)* | Specifies the settings for the `DynamsoftDocumentNormalizer` task. |

### outputOriginalImage

Specifies whether to return the original image in the captured results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) BOOL outputOriginalImage;
```
2. 
```swift
var outputOriginalImage: Bool { get set }
```

**Remarks**

The property determines:

1. Whether the [`CapturedResult`](captured-result.html) object contains the original image.
2. Whether you can receive the original image via [`onOriginalImageResultReceived`](captured-result-receiver.md#onoriginalimageresultreceived).

### roi

Specifies the region of interest (ROI) of the image or frame where the capture and recognition will take place.

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

Specifies whether the ROI is measured in pixels (false) or as a percentage of the image dimensions (true).

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

### minImageCaptureInterval

Set the minimum capture interval (in milliseconds) between consecutive frames when capturing via video. In other words, it is a measure of the frequency in which frames are fetched.

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

**Remarks**

If you find that the battery consumption when using any of the Dynamsoft Capture Vision products, we recommend setting this parameter to a higher value. Please see this [article]({{ site.dbr_ios }}faq/reduce-battery-consumption.html) for more info on how to reduce battery consumption.

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

Specifies the settings for the `DynamsoftBarcodeReader` task with a [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_ios_api }}simplified-barcode-reader-settings.html) object.

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

Specifies the settings for the `DynamsoftLabelRecognizer` task with a [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html) object.

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

Specifies the settings for the `DynamsoftDocumentNormalizer` task with a [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_ios_api }}simplified-document-normalizer-settings.html) object.

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
