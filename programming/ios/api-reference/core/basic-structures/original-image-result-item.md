---
layout: default-layout
title: DSOriginalImageResultItem - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSOriginalImageResultItem of Dynamsoft Capture Vision iOS represents a captured original image result item, which provides an property to get the image data.
keywords: original image result item, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSOriginalImageResultItem

The `OriginalImageResultItem` class extends the [`CapturedResultItem`](captured-result.md) class and represents an original image result item.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSOriginalImageResultItem : DSCapturedResultItem
```
2. 
```swift
class OriginalImageResultItem : CapturedResultItem
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | The image data of the captured original image result item. |

## Inherited Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`type`](captured-result.md#type) | *DSCapturedResultItemType* | The type of the captured result item, indicating what kind of data it represents. |
| [`referenceItem`](captured-result.md#referenceitem) | *DSCapturedResultItem \** | A property of type `DSCapturedResultItem` that represents a reference to another captured result item. |
| [`targetROIDefName`](captured-result.md#targetroidefname) | *NSString* | The name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object which includes a task that generated the result. |
| [`taskName`](captured-result.md#taskname) | *NSString* | The name of the task that generated the result. |

### imageData

The image data of the captured original image result item.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, strong, nullable) DSImageData *imageData;
```
2. 
```swift
var imageData: ImageData { get }
```
