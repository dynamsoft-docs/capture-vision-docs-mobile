---
layout: default-layout
Title: DSBinaryImageUnit - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSBinaryImageUnit of Dynamsoft Core Module represents a unit that contains a binary image.
Keywords: binary image, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSBinaryImageUnit

The `DSBinaryImageUnit` class represents a unit that contains a binary image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSBinaryImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class BinaryImageUnit : IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the binary image. |

### imageData

A `DSImageData` object as the image data of the binary image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable) DSImageData *imageData;
```
2. 
```swift
var imageData: DSImageData? { get set }
```
