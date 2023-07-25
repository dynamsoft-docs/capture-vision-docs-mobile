---
layout: default-layout
Title: ImageManager - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class ImageManager of Dynamsoft Capture Vision Router Module is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.
Keywords: image manager, Java, Kotlin
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

`imageData`: The `ImageData` object to save to an image file.  
`path`: The targeting file path with the file name and extension name.  
`overWrite`: A flag indicating whether to overwrite the file if it already exists. Defaults to true.  

**Exception**

An exception is thrown when the file path is unavailable.

**Return Value**

A boolean value that indicates whether the file is saved successfully.

### drawOnImage(imageData,quads,colour,thickness)

Add quadrilaterals on the image.

```java
ImageData drawOnImage(ImageData imageData, Quadrilateral[] quads, int colour, int thickness){}
```

**Parameters**

`imageData`: The `ImageData` to modify.  
`quads`: An array of `Quadrilateral` objects to be added on the image.  
`colour`: An int value as an ARGB colour.  
`thickness`: The width of the border.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,lineSegments,colour,thickness)

Add lines on the image.

```java
ImageData drawOnImage(ImageData imageData, LineSegment[] lines, int colour, int thickness){}
```

**Parameters**

`imageData`: The `ImageData` to modify.  
`lineSegments`: An array of `LineSegment` objects to be added on the image.  
`colour`: An int value as an ARGB colour.  
`thickness`: The width of the lines.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,contours,colour,thickness)

Add contours on the image.

```java
ImageData drawOnImage(ImageData imageData, Contour[] contours, int colour, int thickness){}
```

**Parameters**

`imageData`: The `ImageData` to modify.  
`contours`: An array of `Contour` objects to be added on the image.  
`colour`: An int value as an ARGB colour.  
`thickness`: The width of the borders.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,corners,colour,thickness)

Add corners on the image.

```java
ImageData drawOnImage(ImageData imageData, Corner[] corners, int colour, int thickness){}
```

**Parameters**

`imageData`: The `ImageData` to modify.  
`corners`: An array of `Corner` objects to be added on the image.  
`colour`: An int value as an ARGB colour.  
`thickness`: The width of the lines.

**Return Value**

The modified `ImageData`.

### drawOnImage(imageData,edges,colour,thickness)

Add edges on the image.

```java
ImageData drawOnImage(ImageData imageData, Edge[] edges, int colour, int thickness){}
```

**Parameters**

`imageData`: The `ImageData` to modify.  
`edges`: An array of `Edge` objects to be added on the image.  
`colour`: An int value as an ARGB colour.  
`thickness`: The width of the lines.  

**Return Value**

The modified `ImageData`.
