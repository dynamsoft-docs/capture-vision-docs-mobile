---
layout: default-layout
title: ImageManager - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class ImageManager of Dynamsoft Capture Vision Router Module is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.
keywords: image manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageManager

The `ImageManager` class is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftUtility.aar

```java
class ImageManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`saveToFile`](#savetofile) | Save an `ImageData` object as an image file. |
| [`drawOnImage(imageData,quads,colour,thickness)`](#drawonimageimagedataquadscolourthickness) | Add quadrilaterals on the image. |
| [`drawOnImage(imageData,lines,colour,thickness)`](#drawonimageimagedatalinesegmentscolourthickness) | Add lines on the image. |
| [`drawOnImage(imageData,contours,colour,thickness)`](#drawonimageimagedatacontourscolourthickness) | Add contours on the image. |
| [`drawOnImage(imageData,corners,colour,thickness)`](#drawonimageimagedatacornerscolourthickness) | Add corners on the image. |
| [`drawOnImage(imageData,edges,colour,thickness)`](#drawonimageimagedataedgescolourthickness) | Add edges on the image. |

### saveToFile

Save an `ImageData` object as an image file.

```java
void saveToFile(ImageData imageData, String path, boolean overWrite) throws UtilityException{}
```

**Parameters**

`[in] imageData`: The `ImageData` object to save to an image file.  

`[in] path`: The targeting file path with the file name and extension name.  

`[in] overWrite`: A flag indicating whether to overwrite the file if it already exists. Defaults to true.  

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**Return Value**

A boolean value that indicates whether the file is saved successfully.

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
