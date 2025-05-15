---
layout: default-layout
title: ImageDrawer - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class ImageDrawer of Dynamsoft Capture Vision Router Module is a utility class for drawing graphics on images.
keywords: image manager, Objective-C, OC, Swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageDrawer

The class `ImageDrawer` is a utility class for drawing graphics on images.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class ImageDrawer
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`drawOnImage(image,quads,colour,thickness)`](#drawonimageimagequadscolourthickness) | Add quadrilaterals on the image. |
| [`drawOnImage(image,lines,colour,thickness)`](#drawonimageimagelinesegmentscolourthickness) | Add lines on the image. |
| [`drawOnImage(image,contours,colour,thickness)`](#drawonimageimagecontourscolourthickness) | Add contours on the image. |
| [`drawOnImage(image,corners,colour,thickness)`](#drawonimageimagecornerscolourthickness) | Add corners on the image. |
| [`drawOnImage(image,edges,colour,thickness)`](#drawonimageimageedgescolourthickness) | Add edges on the image. |

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
