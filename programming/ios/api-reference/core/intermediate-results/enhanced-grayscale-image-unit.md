---
layout: default-layout
Title: DSEnhancedGrayscaleImageUnit - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSEnhancedGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a grayscale enhanced image.
Keywords: enhanced grayscale image unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSEnhancedGrayscaleImageUnit

The `DSEnhancedGrayscaleImageUnit` class represents a unit that contains a grayscale enhanced image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSEnhancedGrayscaleImageUnit : DSIntermediateResultUnit
```
2. 
```swift
class EnhancedGrayscaleImageUnit : IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the grayscale enhanced image. |

### imageData

A `DSImageData` object as the image data of the grayscale enhanced image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSImageData *imageData;
```
2. 
```swift
var imageData: DSImageData? { get set }
```
