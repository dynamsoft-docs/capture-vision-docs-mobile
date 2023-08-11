---
layout: default-layout
Title: Processing a Single Image - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The APIs of the CaptureVisionRouter for processing a single image.
Keywords: capture vision, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing a Single Image

| Method | Description |
| ------ | ----------- |
| [`capture(filePath,templateName)`](#capturefilepathtemplatename) | Capture data from the file specified by the file path. |
| [`capture(fileBytes,templateName)`](#capturefilebytestemplatename) | Capture data from a given file in memory. |
| [`capture(imageData,templateName)`](#captureimagedatatemplatename) | Capture data from the memory buffer via a [`ImageData`](../core/basic-structures/image-data.md) object. |
| [`capture(bitmap,templateName)`](#capturebitmaptemplatename) | Capture data from the given Bitmap. |

## capture(filePath,templateName)

Capture data from the file specified by the file path.

```java
CapturedResult capture(String filePath, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`[in] file`: The file path and name that you want to capture data from.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNG files).

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.

## capture(fileBytes,templateName)

Capture data from a given file in memory.

```java
CapturedResult capture(byte[] fileBytes, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`[in] fileBytes`: A byte array that points to a file in memory.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNGles).

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.

## capture(imageData,templateName)

Capture data from the memory buffer via a [`ImageData`](../core/basic-structures/image-data.md) object.

```java
CapturedResult capture(ImageData imageData, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`[in] buffer`: A [`ImageData`](../core/basic-structures/image-data.md) object that contains image info.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The image buffer is invalid.

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.

## capture(bitmap,templateName)

Capture data from the given Bitmap.

```java
CapturedResult capture(Bitmap bitmap, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`[in] bitmap`: A `android.graphics.Bitmap` object.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.
