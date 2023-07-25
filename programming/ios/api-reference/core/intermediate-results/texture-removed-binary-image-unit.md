---
layout: default-layout
Title: DSTextureRemovedBinaryImageUnit - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSTextureRemovedBinaryImageUnit of Dynamsoft Core Module represents a unit that contains a texture-removed binary image.
Keywords: texture-removed binary image, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextureRemovedBinaryImageUnit

The `DSTextureRemovedBinaryImageUnit` class represents a unit that contains a texture-removed binary image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(TextureRemovedBinaryImageUnit)
@interface DSTextureRemovedBinaryImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class TextureRemovedBinaryImageUnit : IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the texture-removed binary image. |

### imageData

A `DSImageData` object as the image data of the texture-removed binary image.

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
var imageData: ImageData? { get set }
```
