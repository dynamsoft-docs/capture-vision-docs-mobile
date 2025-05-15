---
layout: default-layout
title: FileFetcher - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class FileFetcher of Dynamsoft Capture Vision Router Module is a utility class that partitions a multi-page image file into multiple independent ImageData objects.
keywords: file fetcher, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# FileFetcher

The `FileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits the [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) class so that you can set it as the input of `CaptureVisionRouter` with the API [`setInput`]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#setinput).

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

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
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Whether there is a next image to fetch. |
| [`getImage`](#getimage) | Get the image data of the image. |
| [`setPages`](#setpages) | Set the pages to read. |

The following methods are inherited from [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html).

| Method | Description |
| ------ | ----------- |
| [`addImageToBuffer`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#addimagetobuffer) | Adds an image to the internal buffer. |
| [`clearBuffer`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#clearbuffer) | Clears all images from the buffer, resetting the state for new image fetching. |
| [`getBufferOverflowProtectionMode`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getbufferoverflowprotectionmode) | Get the current mode for handling buffer overflow. |
| [`getColourChannelUsageType`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getcolourchannelusagetype) | Get the current usage type for color channels in images. |
| [`getImageCount`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getimagecount) | Get the current number of images in the buffer. |
| [`getImage`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getimage) | Get a buffered image. Implementing classes should return a Promise that resolves with an instance of `DSImageData`. |
| [`getMaxImageCount`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getmaximagecount) | Get the maximum number of images that can be buffered. |
| [`hasImage`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#hasimage) | Checks if an image with the specified ID is present in the buffer. |
| [`hasNextImageToFetch`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#hasnextimagetofetch) | Determines whether there are more images available to fetch. |
| [`isBufferEmpty`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#isbufferempty) | Determines whether the buffer is currently empty. |
| [`setBufferOverflowProtectionMode`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setbufferoverflowprotectionmode) | Sets the behavior for handling new incoming images when the buffer is full. |
| [`setColourChannelUsageType`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setcolourchannelusagetype) | Sets the usage type for color channels in images. |
| [`setErrorListener`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#seterrorlistener) | Sets an error listener to receive notifications about errors that occur during image source operations. |
| [`setMaxImageCount`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setmaximagecount) | Sets the maximum number of images that can be buffered at any time. |
| [`setNextImageToReturn(imageId)`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setnextimagetoreturnimageid) | Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage. |
| [`setNextImageToReturn(imageId,keepInBuffer)`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setnextimagetoreturnimageidkeepinbuffer) | Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage. |
| [`startFetching`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`stopFetching`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |

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

<!-- 
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
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. | -->

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

### setPages

Set the pages to read.

```java
void setPages(int[] pages) throws UtilityException;
```

**Parameters**

`pages`: An array that contains all the pages to read.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND  | -10005 | File not found. |
| EC_FILE_TYPE_NOT_SUPPORTED  | -10006 | The file type is not supported. |
| EC_IMAGE_READ_FAILED  | -10012 | Failed to read the image. |

## Inherited Methods

The following methods are inherited from the [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) class:

| Method | Description |
| ------ | ----------- |
| [`hasNextImageToFetch`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#hasnextimagetofetch) | Determines whether there are more images left to fetch. |
| [`setMaxImageCount`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setmaximagecount) | Set the maximum capability of the Video Buffer. |
| [`getMaxImageCount`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getmaximagecount) | Get the property defines the maximum capability of the Video Buffer. |
| [`setBufferOverflowProtectionMode`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setbufferoverflowprotectionmode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. You can either block the Video Buffer or push out the oldest image and append a new one. |
| [`getBufferOverflowProtectionMode`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getbufferoverflowprotectionmode) | Get the buffer overflow protection mode. |
| [`getImageCount`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getimagecount) | Get the current image count in the Video Buffer. |
| [`isBufferEmpty`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#isbufferempty) | Check whether the Video Buffer is empty. |
| [`setColourChannelUsageType`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setcolourchannelusagetype) | Set the usage type of a color channel in an image. |
| [`getColourChannelUsageType`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getcolourchannelusagetype) | Get the usage type of a color channel in an image. |
| [`startFetching`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`stopFetching`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`getImage`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#getimage) | Get an image from the Video Buffer. |
| [`setNextImageToReturn(imageId)`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setnextimagetoreturnimageid) | Specify the next image that is returned by method getImage. |
| [`setNextImageToReturn(imageId,keepInBuffer)`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#setnextimagetoreturnimageidkeepinbuffer) | Specify the next image that is returned by method getImage. |
| [`hasImage`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#hasimage) | Check the availability of the specified image. |
| [`addImageToBuffer`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#addimagetobuffer) | Adds an image to the buffer of the adapter. |
| [`clearBuffer`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#clearbuffer) | Clears the image buffer. |
| [`setErrorListener`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html#seterrorlistener) | Clears the image buffer. |
