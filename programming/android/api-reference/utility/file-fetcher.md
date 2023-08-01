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
void setFile(String filePath) throws UtilityException
```

**Parameters**

`[in] filePath`: The file path.

**Exception**

An exception is thrown when fail to load the image.

### setFile(fileBytes)

Sets the file with file bytes.

```java
void setFile(byte[] fileBytes) throws UtilityException
```

**Parameters**

`[in] fileBytes`: The file bytes.  

**Exception**

An exception is thrown when fail to load the image.

### setFile(imageData)

Sets the file with a `ImageData` object.

```java
void setFile(ImageData imageData) throws UtilityException
```

**Parameters**

`[in] buffer`: The image data.

**Exception**

An exception is thrown when fail to load the image.

### setFile(bitmap)

Sets the file with an `android.graphics.Bitmap`.

```java
void setFile(Bitmap bitmap) throws UtilityException
```

**Parameters**

`[in] image`: An `android.graphics.Bitmap`.

**Exception**

An exception is thrown when fail to load the image.

### setPDFReadingParameter

Sets the parameters of PDF reading.

```java
void setPDFReadingParameter(PDFReadingParameter para) throws UtilityException
```

**Parameters**

`[in] para`: The parameter object for reading PDF files.

### hasNextImageToFetch

Whether there is a next image to fetch.

```java
boolean hasNextImageToFetch()
```

**Return Value**

A boolean value that indicates whether there is a next image to fetch.

### getImage

Get the image data of the image.

```java
ImageData getImage()
```

**Return Value**

A `ImageData` as the image.
