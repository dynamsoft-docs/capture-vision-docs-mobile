---
layout: default-layout
title: FileFetcher * Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class FileFetcher of Dynamsoft Capture Vision Router Module is a utility class that partitions a multi-page image file into multiple independent ImageData objects.
keywords: file fetcher, Java, Kotlin
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

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |

### setFile(fileBytes)

Sets the file with file bytes.

```java
void setFile(byte[] fileBytes) throws UtilityException
```

**Parameters**

`[in] fileBytes`: The file bytes.  

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |

### setFile(imageData)

Sets the file with a `ImageData` object.

```java
void setFile(ImageData imageData) throws UtilityException
```

**Parameters**

`[in] buffer`: The image data.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |

### setFile(bitmap)

Sets the file with an `android.graphics.Bitmap`.

```java
void setFile(Bitmap bitmap) throws UtilityException
```

**Parameters**

`[in] image`: An `android.graphics.Bitmap`.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The image data of the Bitmap is null. |

### setPDFReadingParameter

Sets the parameters of PDF reading.

```java
void setPDFReadingParameter(PDFReadingParameter para) throws UtilityException
```

**Parameters**

`[in] para`: The parameter object for reading PDF files.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |

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
