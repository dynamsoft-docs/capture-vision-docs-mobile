---
layout: default-layout
Title: FileFetcher * Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class FileFetcher of Dynamsoft Capture Vision Router Module is a utility class that partitions a multi-page image file into multiple independent ImageData objects.
Keywords: file fetcher, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# FileFetcher

The `FileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `ImageSourceAdapter` class.

## Definition

*Namespace:* com.dynamsoft.utility  
*Assembly:* DynamsoftUtility.aar

```java
class FileFetcher
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`setFile(filePath)`](#setfilefilepath) | Sets the file with a file path. |
| [`setFile(fileBytes)`](#setfilefilebytes) | Sets the file with file bytes. |
| [`setFile(imageData)`](#setfileimagedata) | Sets the file with a `ImageData` object. |
| [`setFile(bitmap)`](#setfilebitmap) | Sets the file with a `Bitmap`. |
| [`setPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters of PDF reading. |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Whether there is a next image to fetch. |
| [`getImage`](#getimage) | Get the image data of the image. |

### setFile(filePath)

Sets the file with a file path.

```java
void setFile(String filePath) throws UtilityException{}
```

**Parameters**

`filePath`: The file path.

**Exception**

An exception is thrown when fail to load the image.

### setFile(fileBytes)

Sets the file with file bytes.

```java
void setFile(byte[] fileBytes) throws UtilityException{}
```

**Parameters**

`fileBytes`: The file bytes.  
**Exception**

An exception is thrown when fail to load the image.

### setFile(imageData)

Sets the file with a `ImageData` object.

```java
void setFile(ImageData imageData) throws UtilityException{}
```

**Parameters**

`buffer`: The image data.

**Exception**

An exception is thrown when fail to load the image.

### setFile(bitmap)

Sets the file with an `android.graphics.Bitmap`.

```java
void setFile(Bitmap bitmap) throws UtilityException{}
```

**Parameters**

`image`: An `android.graphics.Bitmap`.

**Exception**

An exception is thrown when fail to load the image.

### setPDFReadingParameter

Sets the parameters of PDF reading.

```java
func setPDFReadingParameter(_ para: PDFReadingParameter) throws
```

**Parameters**

`para`: The parameter object for reading PDF files.

**Exception**

An exception is thrown when:

* The directory is unavailable.
* The method is triggered after the capture is started.

**Return Value**

A boolean value that indicates whether the PDF reading mode is set successfully.

### hasNextImageToFetch

Whether there is a next image to fetch.

```java
func hasNextImageToFetch() -> Bool
```

**Return Value**

A boolean value that indicates whether there is a next image to fetch.

### getImage

Get the image data of the image.

```java
func getImage() -> ImageData
```

**Return Value**

A `ImageData` as the image.
