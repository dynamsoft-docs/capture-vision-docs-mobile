---
layout: default-layout
title: DSImageData - Dynamsoft Core Module iOS Edition API Reference
description: The class DSImageData of Dynamsoft Core Module represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.
keywords: image data, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageData

The `DSImageData` class defines the structure of an object that represents an image.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSImageData : NSObject
```
2. 
```swift
class ImageData : NSObject
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`bytes`](#bytes) | *NSData \** | The image data content in a byte array. |
| [`width`](#width) | *NSInteger* | The width of the image in pixels. |
| [`height`](#height) | *NSInteger* | The height of the image in pixels. |
| [`stride`](#stride) | *NSInteger* | The stride (or scan width) of the image. |
| [`format`](#format) | *DSImagePixelFormat* | The image pixel format used in the image byte array. |
| [`orientation`](#orientation) | *NSInteger* | The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file. |
| [`tag`](#tag) | *DSImageTag \** | The tag of the image. |

| Method | Description |
| ------ | ----------- |
| [`toUIImage`](#touiimage) | Transform the DSImageData to a UIImage. |

### bytes

The image data content in a byte array.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, copy) NSData *bytes;
```
2. 
```swift
var bytes: Data? { get set }
```

### width

The width of the image in pixels.  

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSUInteger width
```
2. 
```swift
var width: Int { get set }
```

### height

The height of the image in pixels.  

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSUInteger height
```
2. 
```swift
var height: Int { get set }
```

### stride

The stride (or scan width) of the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSUInteger stride
```
2. 
```swift
var stride: Int { get set }
```

### format

The image pixel format used in the image byte array.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSImagePixelFormat format
```
2. 
```swift
var format: DSImagePixelFormat { get set }
```

### orientation

The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger orientation
```
2. 
```swift
var orientation: Int { get set }
```

### tag

The tag of the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSImageTag *tag;
```
2. 
```swift
var tag?: DSImageTag { get set }
```

### toUIImage

Transform the DSImageData to a UIImage.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable UIImage *)toUIImage:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func toUIImage() throws -> UIImage
```

**Parameters**

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_BPP_NOT_SUPPORTED | -10007 | The pixel format is not supported or the ImageData is invalid. |

**Return Value**

A `UIImage` that converted from the `DSImageData`.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSError *error;
UIImage *image = [imageData toUIImage:&error];
```
2. 
```swift
do{
   image = try imageData.toUIImage()
} catch{
   // Add your code to deal with exceptions.
}
```
