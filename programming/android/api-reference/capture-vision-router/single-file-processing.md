---
layout: default-layout
title: Processing a Single Image - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The APIs of the CaptureVisionRouter for processing a single image.
keywords: capture vision, Java, Kotlin
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
CapturedResult capture(String filePath, String templateName);
```

**Parameters**

`[in] file`: The file path and name that you want to capture data from.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## capture(fileBytes,templateName)

Capture data from a given file in memory.

```java
CapturedResult capture(byte[] fileBytes, String templateName);
```

**Parameters**

`[in] fileBytes`: A byte array that points to a file in memory.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## capture(imageData,templateName)

Capture data from the memory buffer via a [`ImageData`](../core/basic-structures/image-data.md) object.

```java
CapturedResult capture(ImageData imageData, String templateName);
```

**Parameters**

`[in] buffer`: A [`ImageData`](../core/basic-structures/image-data.md) object that contains image info.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## capture(bitmap,templateName)

Capture data from the given Bitmap.

```java
CapturedResult capture(Bitmap bitmap, String templateName);
```

**Parameters**

`[in] bitmap`: A `android.graphics.Bitmap` object.

`[in] templateName`: Specify a template with a template name for the data capturing.

**Return Value**

A [`CapturedResult`](../core/basic-structures/captured-result.md) object output by the library.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |
