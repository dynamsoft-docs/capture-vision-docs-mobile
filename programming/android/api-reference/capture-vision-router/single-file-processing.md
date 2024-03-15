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

This page introduces the `capture` APIs of the `CaptureVisionRouter` that designed for processing a single image (or single page file).

> Note:
>
> - [Use the `DirectoryFetcher` to process a set of image files]({{ site.dcv_android_api }}utility/directory-fetcher.html).
> - [Use the `FileFetcher` to process the multi-page files such as PDF and TIFF]({{ site.dcv_android_api }}utility/file-fetcher.html).

| Method | Description |
| ------ | ----------- |
| [`capture(filePath,templateName)`](#capturefilepathtemplatename) | Processes a single image or a file containing a single image to derive important information with the file path. |
| [`capture(fileBytes,templateName)`](#capturefilebytestemplatename) | Processes a single image or a file containing a single image to derive important information with the file bytes in the memory. |
| [`capture(imageData,templateName)`](#captureimagedatatemplatename) | Processes a single image or a file containing a single image to derive important information with an [`ImageData`](../core/basic-structures/image-data.md) object. |
| [`capture(bitmap,templateName)`](#capturebitmaptemplatename) | Processes a single image or a file containing a single image to derive important information with a `Bitmap`. |

## capture(filePath,templateName)

Processes a single image or a file containing a single image to derive important information with the file path.

```java
CapturedResult capture(String filePath, String templateName);
```

**Parameters**

`[in] file`: The file path and name that you want to capture data from.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?lang=android) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`CapturedResult`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result.html) object which contains the derived information from the image processed.

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

Processes a single image or a file containing a single image to derive important information with the file bytes in the memory.

```java
CapturedResult capture(byte[] fileBytes, String templateName);
```

**Parameters**

`[in] fileBytes`: A byte array that points to a file in memory.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?lang=android) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`CapturedResult`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result.html) object which contains the derived information from the image processed.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## capture(imageData,templateName)

Processes a single image or a file containing a single image to derive important information with an [`ImageData`]({{ site.dcv_android_api }}core/basic-structures/image-data.html) object.

```java
CapturedResult capture(ImageData imageData, String templateName);
```

**Parameters**

`[in] buffer`: A [`ImageData`]({{ site.dcv_android_api }}core/basic-structures/image-data.html) object that contains image info.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?lang=android) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`CapturedResult`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result.html) object which contains the derived information from the image processed.

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

Processes a single image or a file containing a single image to derive important information with a `Bitmap`.

```java
CapturedResult capture(Bitmap bitmap, String templateName);
```

**Parameters**

`[in] bitmap`: A `android.graphics.Bitmap` object.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?lang=android) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`CapturedResult`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result.html) object which contains the derived information from the image processed.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |
