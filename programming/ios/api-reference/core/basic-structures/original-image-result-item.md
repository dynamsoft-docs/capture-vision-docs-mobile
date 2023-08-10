---
layout: default-layout
Title: DSOriginalImageResultItem - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSOriginalImageResultItem of Dynamsoft Core Module represents a captured original image result item, which provides an property to get the image data.
Keywords: original image result item, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSOriginalImageResultItem

The `DSOriginalImageResultItem` class represents a captured original image result item, which is a derived class of `DSCapturedResultItem` and provides a property to get the image data.

## Definition

*Assembly:* DynamsoftCore.framework

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

### imageData

The image data of the captured original image result item.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nonnull, readonly) DSImageData* imageData;
```
2. 
```swift
var imageData: ImageData { get }
```
