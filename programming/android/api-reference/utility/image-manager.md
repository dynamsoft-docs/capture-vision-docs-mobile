---
layout: default-layout
Title: DSImageManager - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class DSImageManager of Dynamsoft Capture Vision Router Module is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.
Keywords: image manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageManager

The `DSImageManager` class is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.

## Definition

*Namespace*: com.dynamsoft.utility  
*Assembly:* DynamsoftUtility.aar

```java
class ImageManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`saveToFile`](#savetofile) | Save an `ImageData` object as an image file. |
| [`drawOnImage(image,quads,colour,thickness)`](#drawonimageimagequadscolourthickness) | Add quadrilaterals on the image. |
| [`drawOnImage(image,lines,colour,thickness)`](#drawonimageimagelinesegmentscolourthickness) | Add lines on the image. |
| [`drawOnImage(image,contours,colour,thickness)`](#drawonimageimagecontourscolourthickness) | Add contours on the image. |
| [`drawOnImage(image,corners,colour,thickness)`](#drawonimageimagecornerscolourthickness) | Add corners on the image. |
| [`drawOnImage(image,edges,colour,thickness)`](#drawonimageimageedgescolourthickness) | Add edges on the image. |

### saveToFile

Save an `ImageData` object as an image file.

```java
func save(toFile imageData: ImageData, path: String, overWrite: Bool) throws -> Bool
```

**Parameters**

`imageData`: The `ImageData` object to save to an image file.  
`path`: The targeting file path with the file name and extension name.  
`overWrite`: A flag indicating whether to overwrite the file if it already exists. Defaults to true.  
`error`: A `NSError` pointer. An error occurs when the file path is unavailable.

**Return Value**

A `BOOL` value that indicates whether the file is saved successfully.

### drawOnImage(image,quads,colour,thickness)

Add quadrilaterals on the image.

```java
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

```java
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

```java
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

```java
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

```java
func drawOnImage(_ image: ImageData, edges: [Edge], colour: UIColor, thickness: Int) -> ImageData
```

**Parameters**

`image`: The `ImageData` to modify.  
`edges`: An array of `DSEdge` objects to be added on the image.  
`colour`: A `UIColor` that specifies the targeting colour.  
`thickness`: The width of the lines.  

**Return Value**

The modified `ImageData`.
