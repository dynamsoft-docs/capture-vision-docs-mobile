---
layout: default-layout
title: Single Image Processing - Dynamsoft Capture Vision MAUI Edition
description: The APIs of the CaptureVisionRouter MAUI edition for processing a single image - Dynamsoft Capture Vision MAUI Edition
keywords: capture, single, CapturedResult
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing a Single Image

This page introduces the `capture` APIs of the `CaptureVisionRouter` that designed for processing a single image (or single page file).

| Method | Description |
| ------ | ----------- |
| [`Capture(filePath)`](#capturefilepath) | Processes a single image or a file containing a single image to derive important information with the file path. |
| [`Capture(fileBytes)`](#capturefilebytes) | Processes a single image in the memory with the fileBytes. |
| [`Capture(imageData)`](#captureimagedata) | Processes a single image with the `ImageData`. |

## Capture(filePath)

Processes a single image or a file containing a single image to derive important information with the file path.

> Note: The file should be a single image or a single page image file.

```csharp
CapturedResult Capture(string filePath, string templateName);
```

**Parameters**

`[in] filePath`: The file path and name that you want to capture data from.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/preset-template.html) member. This is available only if you have never upload a new template via [`InitSettings`](settings.md#initsettings) or [`InitSettingsFromFile`](settings.md#initsettingsfromfile).
- A string that represents one of the template name that you have uploaded via `InitSettings` or `InitSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `InitSettingsFromFile` or `InitSettings`.

**Return Value**

A [`CapturedResult`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result.html) object which contains the derived information from the image processed.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## Capture(fileBytes)

Processes a single image in the memory with the fileBytes.

> Note: The file should be a single image or a single page image file.

```csharp
CapturedResult Capture(byte[] fileBytes, string templateName);
```

**Parameters**

`[in] fileBytes`: The fileBytes of the file in memory.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/preset-template.html) member. This is available only if you have never upload a new template via [`InitSettings`](settings.md#initsettings) or [`InitSettingsFromFile`](settings.md#initsettingsfromfile).
- A string that represents one of the template name that you have uploaded via `InitSettings` or `InitSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `InitSettingsFromFile` or `InitSettings`.

**Return Value**

A [`CapturedResult`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result.html) object which contains the derived information from the image processed.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## Capture(imageData)

Processes a single image with the `ImageData`.

```csharp
CapturedResult Capture(ImageData imageData, string templateName);
```

**Parameters**

`[in] imageData`: The `ImageData` of the image.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/preset-template.html) member. This is available only if you have never upload a new template via [`InitSettings`](settings.md#initsettings) or [`InitSettingsFromFile`](settings.md#initsettingsfromfile).
- A string that represents one of the template name that you have uploaded via `InitSettings` or `InitSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `InitSettingsFromFile` or `InitSettings`.

**Return Value**

A [`CapturedResult`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result.html) object which contains the derived information from the image processed.

If an error occurs when processing the image, the `CapturedResult` object will include error code and error message that describes the reason of the error.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |
