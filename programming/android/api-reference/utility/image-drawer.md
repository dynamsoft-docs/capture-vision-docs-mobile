---
layout: default-layout
title: ImageDrawer - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class ImageDrawer of Dynamsoft Capture Vision Router Module is a utility class for drawing graphics on images.
keywords: image manager, Java, Kotlin
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
| [`drawOnImage(imageData,quads,colour,thickness)`](#drawonimageimagedataquadscolourthickness) | Add quadrilaterals on the image. |
| [`drawOnImage(imageData,lines,colour,thickness)`](#drawonimageimagedatalinesegmentscolourthickness) | Add lines on the image. |
| [`drawOnImage(imageData,contours,colour,thickness)`](#drawonimageimagedatacontourscolourthickness) | Add contours on the image. |
| [`drawOnImage(imageData,corners,colour,thickness)`](#drawonimageimagedatacornerscolourthickness) | Add corners on the image. |
| [`drawOnImage(imageData,edges,colour,thickness)`](#drawonimageimagedataedgescolourthickness) | Add edges on the image. |

### drawOnImage(imageData,quads,colour,thickness)

Add quadrilaterals on the image.

```java
ImageData drawOnImage(ImageData imageData, Quadrilateral[] quads, int colour, int thickness){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.  

`[in] quads`: An array of `Quadrilateral` objects to be added on the image.  

`[in] colour`: An int value as an ARGB colour.  

`[in] thickness`: The width of the border.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,lineSegments,colour,thickness)

Add lines on the image.

```java
ImageData drawOnImage(ImageData imageData, LineSegment[] lines, int colour, int thickness){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.  

`[in] lineSegments`: An array of `LineSegment` objects to be added on the image.  

`[in] colour`: An int value as an ARGB colour.  

`[in] thickness`: The width of the lines.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,contours,colour,thickness)

Add contours on the image.

```java
ImageData drawOnImage(ImageData imageData, Contour[] contours, int colour, int thickness){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.  

`[in] contours`: An array of `Contour` objects to be added on the image.  

`[in] colour`: An int value as an ARGB colour.  

`[in] thickness`: The width of the borders.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,corners,colour,thickness)

Add corners on the image.

```java
ImageData drawOnImage(ImageData imageData, Corner[] corners, int colour, int thickness){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.  

`[in] corners`: An array of `Corner` objects to be added on the image.  

`[in] colour`: An int value as an ARGB colour.  

`[in] thickness`: The width of the lines.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,edges,colour,thickness)

Add edges on the image.

```java
ImageData drawOnImage(ImageData imageData, Edge[] edges, int colour, int thickness){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify. 

`[in] edges`: An array of `Edge` objects to be added on the image.  

`[in] colour`: An int value as an ARGB colour.  

`[in] thickness`: The width of the lines.  

**Return Value**

The modified `ImageData`.
