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
| [`capture(filePath,templateName)`](#capturefilepathtemplatename) | Implement data capture on the given file. |
| [`capture(fileBytes,templateName)`](#capturefilebytestemplatename) | Implement data capture on the given file in memory. |
| [`capture(imageData,templateName)`](#captureimagedatatemplatename) | Implement data capture on the given image data. |
| [`capture(bitmap,templateName)`](#capturebitmaptemplatename) | Implement data capture on the given Bitmap. |

## capture(filePath,templateName)

Implement data capture on the given file.

```java
CapturedResult capture(String filePath, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`file`: The file path and name that you want to implement the data capturing.
`templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNG files).

**Return Value**

A `CapturedResult` object output by the library.

## capture(fileBytes,templateName)

Implement data capture on the given file in memory.

```java
CapturedResult capture(byte[] fileBytes, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`fileBytes`: A byte array that points to a file in memory.
`templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNGles).

**Return Value**

A `CapturedResult` object output by the library.

## capture(imageData,templateName)

Implement data capture on the given file.

```java
CapturedResult capture(ImageData imageData, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`buffer`: A `ImageData` object that contains image info.
`templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The image buffer is invalid.

**Return Value**

A `CapturedResult` object output by the library.

## capture(bitmap,templateName)

Implement data capture on the given file.

```java
CapturedResult capture(Bitmap bitmap, String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`bitmap`: A `android.graphics.Bitmap` object.
`templateName`: Specify a template with a template name for the data capturing.

**Exception**

An exception is thrown if:

* The method is triggered after the capture is started.
* The template name you input is invalid.

**Return Value**

A `CapturedResult` object output by the library.
