---
layout: default-layout
title: DSImageManager - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSImageManager of Dynamsoft Capture Vision Router Module is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.
keywords: image manager, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageManager

The `DSImageManager` class is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.

## Definition

*Assembly:* DynamsoftUtility.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSImageManager : NSObject
```
2. 
```swift
class ImageManager : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`saveToFile`](#savetofile) | Saves an image to the specified path and format. |
| [`drawOnImage(image,quads,colour,thickness)`](#drawonimageimagequadscolourthickness) | Add quadrilaterals on the image. |
| [`drawOnImage(image,lines,colour,thickness)`](#drawonimageimagelinesegmentscolourthickness) | Add lines on the image. |
| [`drawOnImage(image,contours,colour,thickness)`](#drawonimageimagecontourscolourthickness) | Add contours on the image. |
| [`drawOnImage(image,corners,colour,thickness)`](#drawonimageimagecornerscolourthickness) | Add corners on the image. |
| [`drawOnImage(image,edges,colour,thickness)`](#drawonimageimageedgescolourthickness) | Add edges on the image. |

### saveToFile

Saves an image to the specified path and format. The desired file format is inferred from the file extension provided in the `path` parameter.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)saveToFile:(DSImageData *)imageData
              path:(NSString *)path
         overWrite:(BOOL)overWrite
             error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func save(toFile imageData: ImageData, path: String, overWrite: Bool) throws -> Bool
```

**Parameters**

`imageData`: The image to be saved, of type `ImageData`.

`path`: The file path, name and extension name, as a string, under which the image will be saved.

`overWrite`: A flag indicating whether to overwrite the file if it already exists. Defaults to true.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**Return Value**

A `BOOL` value that indicates whether the file is saved successfully.

### drawOnImage(image,quads,colour,thickness)

Add quadrilaterals on the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)drawOnImage:(DSImageData *)image
                       quads:(NSArray<DSQuadrilateral *> *)quads
                      colour:(UIColor)colour
                   thickness:(NSInteger)thickness;
```
2. 
```swift
func drawOnImage(_ image: ImageData, quads: [Quadrilateral], colour: UIColor, thickness: Int) -> ImageData
```
**Parameters**

`image`: The `ImageData` to modify.

`quads`: An array of `Quadrilateral` objects to be added on the image.

`colour`: A `UIColor` that specifies the targeting colour.

`thickness`: The width of the border.

**Return Value**

The modified `ImageData`.

### drawOnImage(image,lineSegments,colour,thickness)

Add lines on the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)drawOnImage:(DSImageData *)image
                lineSegments:(NSArray<DSLineSegment *> *)lineSegments
                      colour:(UIColor)colour
                   thickness:(NSInteger)thickness;
```
2. 
```swift
func drawOnImage(_ image: ImageData, lineSegments: [LineSegment], colour: UIColor, thickness: Int) -> ImageData
```
**Parameters**

`image`: The `ImageData` to modify.

`lineSegments`: An array of `LineSegment` objects to be added on the image.

`colour`: A `UIColor` that specifies the targeting colour.

`thickness`: The width of the lines.

**Return Value**

The modified `ImageData`.

### drawOnImage(image,contours,colour,thickness)

Add contours on the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)drawOnImage:(DSImageData *)image
                    contours:(NSArray<DSContour *> *)contours
                      colour:(UIColor)colour
                   thickness:(NSInteger)thickness;
```
2. 
```swift
func drawOnImage(_ image: ImageData, contours: [Contour], colour: UIColor, thickness: Int) -> ImageData
```
**Parameters**

`image`: The `ImageData` to modify.

`contours`: An array of `Contour` objects to be added on the image.

`colour`: A `UIColor` that specifies the targeting colour.

`thickness`: The width of the borders.

**Return Value**

The modified `ImageData`.

### drawOnImage(image,corners,colour,thickness)

Add corners on the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)drawOnImage:(DSImageData *)image
                     corners:(NSArray<DSCorner *> *)corners
                      colour:(UIColor)colour
                   thickness:(NSInteger)thickness;
```
2. 
```swift
func drawOnImage(_ image: ImageData, corners: [Corner], colour: UIColor, thickness: Int) -> ImageData
```
**Parameters**

`image`: The `ImageData` to modify.

`corners`: An array of `Corner` objects to be added on the image.

`colour`: A `UIColor` that specifies the targeting colour.

`thickness`: The width of the lines.

**Return Value**

The modified `ImageData`.

### drawOnImage(image,edges,colour,thickness)

Add edges on the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)drawOnImage:(DSImageData *)image
                       edges:(NSArray<DSEdge *> *)edges
                      colour:(UIColor)colour
                   thickness:(NSInteger)thickness;
```
2. 
```swift
func drawOnImage(_ image: ImageData, edges: [Edge], colour: UIColor, thickness: Int) -> ImageData
```

**Parameters**

`image`: The `ImageData` to modify.  
`edges`: An array of `DSEdge` objects to be added on the image.  
`colour`: A `UIColor` that specifies the targeting colour.  
`thickness`: The width of the lines.  

**Return Value**

The modified `ImageData`.
