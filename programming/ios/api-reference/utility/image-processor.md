---
layout: default-layout
title: ImageProcessor - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class ImageProcessor of Dynamsoft Capture Vision Router Module is a utility class for processing images. It provides functionality like croping or converting images.
keywords: image io, image manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageProcessor

The class `ImageProcessor` is a utility class for managing the image data. It provides functionality for saving images to files and reading images from files.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSImageProcessor : NSObject
```
2. 
```swift
class ImageProcessor : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`cropImage(imageData,rect)`](#cropimageimagedatarect) | Crops an image based on the provided rectangle or quadrilateral. |
| [`cropAndDeskewImage(imageData,quad,dstWidth,dstHeight,padding)`](#cropanddeskewimageimagedataquaddstwidthdstheightpaddingerrorcode) | Crops and deskew an image based on the provided quadrilateral and additional information. |
| [`cropAndDeskewImage(imageData,quad)`](#cropanddeskewimageimagedataquad) | Crops and deskew an image based on the provided quadrilateral. |
| [`adjust(imageData,brightness)`](#adjustbrightness) | Adjusts the brightness of an image. |
| [`adjust(imageData,contrast)`](#adjustcontrast) | Adjusts the contrast of an image. |
| [`filterImage`](#filterimage) | Applies a filter to an image. |
| [`convertToGray(imageData)`](#converttograyimagedata) | Converts an image to grayscale. |
| [`convertToGray(imageData,rgb)`](#converttograyimagedatargb) | Converts an image to grayscale. |
| [`convertToBinaryGlobal(imageData)`](#converttobinaryglobalimagedata) | Converts an image to binary using a global threshold. |
| [`convertToBinaryGlobal(imageData,threshold,invert)`](#converttobinaryglobalimagedatathresholdinvert) | Converts an image to binary using a global threshold. |
| [`convertToBinaryLocal(imageData)`](#converttobinarylocalimagedata) | Converts an image to binary using a local threshold. |
| [`convertToBinaryLocal(imageData,blockSize,compensation,invert)`](#converttobinarylocalimagedatablocksizecompensationinvert) | Converts an image to binary using a local threshold. |

### cropImage(imageData,rect,error)

Crops an image based on the provided rectangle.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)cropImage:(DSImageData *)imageData
                      rect:(DSRect *)rect
                     error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func cropImage(imageData: ImageData, rect: Rect, error: UnsafeMutablePointer<NSError?>?) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`rect`: The `Rect` to crop the image.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Return Value**

The cropped `ImageData`.

### cropAndDeskewImage(imageData,quad,dstWidth,dstHeight,padding)

Crops and deskews an image based on the provided quadrilateral and additional information.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable ImageData*)cropAndDeskewImage:(DSImageData*)imageData
                                     quad:(DSQuadrilateral*)quad
                                 dstWidth:(NSInteger)dstWidth
                                dstHeight:(NSInteger)dstHeight
                                  padding:(NSInteger)padding
                                    error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func cropAndDeskewImage(imageData: ImageData, quad: Quadrilateral, dstWidth: Int, dstHeight: Int, padding: Int) throws -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`quad`: The `Quadrilateral` to crop the image.

`dstWidth`: The width of the destination image.

`dstHeight`: The height of the destination image.

`padding`: The padding value.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

### cropAndDeskewImage(imageData,quad)

Crops and deskews an image based on the provided quadrilateral. The arguments dstWidth, dstHeight, and padding are set to 0.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable ImageData*)cropAndDeskewImage:(DSImageData*)imageData
                                     quad:(DSQuadrilateral*)quad;
                                    error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func cropAndDeskewImage(imageData: ImageData, quad: Quadrilateral) throws -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`quad`: The `Quadrilateral` to crop the image.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

### adjust(imageData,brightness)

Adjusts the brightness of an image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)adjust:(DSImageData *)imageData
             brightness:(NSInteger)brightness;
```
2. 
```swift
func adjust(imageData: ImageData, brightness: Int) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`brightness`: The amount to adjust the brightness by.

**Return Value**

The modified `ImageData`.

### adjust(imageData,contrast)

Adjusts the contrast of an image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)adjust:(DSImageData *)imageData
               contrast:(NSInteger)contrast;
```
2. 
```swift
func adjust(imageData: ImageData, contrast: Int) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`contrast`: The amount to adjust the contrast by.

**Return Value**

The modified `ImageData`.

### filterImage

Applies a filter to an image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)filterImage:(DSImageData *)imageData
                  filterType:(DSFilterType)filterType;
```
2. 
```swift
func filterImage(imageData: ImageData, filterType: FilterType) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`filterType`: The type of filter to apply.

**Return Value**

The modified `ImageData`.

### convertToGray(imageData)

Converts an image to grayscale.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)convertToGray:(DSImageData *)imageData;
```
2. 
```swift
func convertToGray(imageData: ImageData) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

**Return Value**

The converted grayscale `ImageData`.

### convertToGray(imageData,r,g,b)

Converts an image to grayscale.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)convertToGray:(DSImageData *)imageData
                             r:(CGFloat)r
                             g:(CGFloat)g
                             b:(CGFloat)b;
```
2. 
```swift
func convertToGray(imageData: ImageData, r: Float, g: Float, b: Float) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`r`: The weight for the red channel.

`g`: The weight for the green channel.

`b`: The weight for the blue channel.

**Return Value**

The converted grayscale `ImageData`.

### convertToBinaryGlobal(imageData)

Converts an image to binary using a global threshold.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)convertToBinaryGlobal:(DSImageData *)imageData;
```
2. 
```swift
func convertToBinaryGlobal(imageData: ImageData) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

**Return Value**

The converted binary `ImageData`.

### convertToBinaryGlobal(imageData,threshold,invert)

Converts an image to binary using a global threshold.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)convertToBinaryGlobal:(DSImageData *)imageData
                             threshold:(NSInteger)threshold
                                invert:(BOOL)invert;
```
2. 
```swift
func convertToBinaryGlobal(imageData: ImageData, threshold: Int, invert: Bool) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`threshold`: The threshold value.

`invert`: Whether to invert the binary image.

**Return Value**

The converted binary `ImageData`.

### convertToBinaryLocal(imageData)

Converts an image to binary using a local threshold.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)convertToBinaryLocal:(DSImageData *)imageData;
```
2. 
```swift
func convertToBinaryLocal(imageData: ImageData) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

**Return Value**

The converted binary `ImageData`.

### convertToBinaryLocal(imageData,blockSize,compensation,invert)

Converts an image to binary using a local threshold.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)convertToBinaryLocal:(DSImageData *)imageData
                            blockSize:(NSInteger)blockSize
                         compensation:(NSInteger)compensation
                               invert:(BOOL)invert;
```
2. 
```swift
func convertToBinaryLocal(imageData: ImageData, blockSize: Int, compensation: Int, invert: Bool) -> ImageData
```

**Parameters**

`imageData`: The `ImageData` to modify.

`blockSize`: The block size for local thresholding.

`compensation`: The compensation value for local thresholding.

`invert`: Whether to invert the binary image.

**Return Value**

The converted binary `ImageData`.
