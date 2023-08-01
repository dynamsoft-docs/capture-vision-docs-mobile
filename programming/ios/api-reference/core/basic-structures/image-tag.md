---
layout: default-layout
Title: DSImageTag - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSImageTag of Dynamsoft Core Module represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.
Keywords: image tag, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageTag

The `DSImageTag` class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSImageTag : NSObject
```
2. 
```swift
class ImageTag : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageId`](#imageid) | *NSInteger* | The ID of the image. |
| [`type`](#type) | *DSImageTagType* | The type of the image tag. |
| [`distanceMode`](#distancemode) | *DSImageCaptureDistanceMode* | The capture distance mode of the image. |

### imageId

The ID of the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) NSInteger imageId;
```
2. 
```swift
var imageId: Int { get }
```

### type

The type of the image tag.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) EnumImageTagType type;
```
2. 
```swift
var type: EnumImageTagType { get }
```

### distanceMode

The capture distance mode of the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign) EnumImageCaptureDistanceMode distanceMode;
```
2. 
```swift
var distanceMode: EnumImageCaptureDistanceMode { get set }
```
