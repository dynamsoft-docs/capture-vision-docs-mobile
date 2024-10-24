---
layout: default-layout
title: Multiple Images/Pages Processing - Dynamsoft Capture Vision MAUI Edition
description: The APIs of the CaptureVisionRouter MAUI edition for processing multiple Images/Pages.
keywords: Set input, start capturing, result receiver, CRR
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`SetInput`](#setinput) | Sets up an image source to provide images for continuous processing. |
| [`GetInput`](#getinput) | Returns the image source object. |
| [`AddResultReceiver`](#addresultreceiver) | Adds a `ICapturedResultReceiver` object as the receiver of captured results. |
| [`RemoveResultReceiver`](#removeresultreceiver) | Removes the specified CapturedResultReceiver object. |
| [`StartCapturing`](#startcapturing) | Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source. |
| [`StopCapturing`](#stopcapturing) | Stops the capturing process. |
| [`AddResultFilter`](#addresultfilter) | Adds a `CaptureResultFilter` object to filter non-essential results. |
| [`RemoveResultFilter`](#removeresultfilter) | Removes the specified `CaptureResultFilter` object. |

## SetInput

Sets up an image source to provide images for continuous processing.

```csharp
void SetInput(ImageSourceAdapter adapter);
```

**Parameters**

`[in] adapter`: An object of [`ImageSourceAdapter`]({{ site.dcv_maui_api }}core/image-source-adapter.html).

> Note: You can use an object of [`CameraEnhancer`]({{ site.dce_maui_api }}camera-enhancer.html) as the `ImageSourceAdapter` object.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## GetInput

Returns the image source object.

```csharp
ImageSourceAdapter GetInput();
```

**Return Value**

The `ImageSourceAdapter` object that is bind with this `CaptureVisionRouter` object.

## AddResultReceiver

Adds a [`ICapturedResultReceiver`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object as the receiver of captured results.

```csharp
void AddResultReceiver(ICapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: The receiver object, of type [`ICapturedResultReceiver`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

## RemoveResultReceiver

Removes the specified [`ICapturedResultReceiver`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object.

```csharp
void RemoveResultReceiver(ICapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: The receiver object, of type [`ICapturedResultReceiver`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

## StartCapturing

Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source.

```csharp
void StartCapturing(string templateName, ICompletionListener completionHandler);
```

**Parameters**

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/preset-template.html) member. This is available only if you have never upload a new template via `InitSettings` or `InitSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `InitSettings` or `InitSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `InitSettingsFromFile` or `InitSettings`.

`[in] completionHandler`: A [`CompletionListener`]({{ site.dcv_maui_api }}core/completion-listener.html) the system calls after it finishes the `StartCapturing`.

## StopCapturing

Stops the capturing process.

```csharp
void StopCapturing();
```

## AddResultFilter

Adds a `CapturedResultFilter` object to filter non-essential results. Currnetly, [`MultiFrameCrossFilter`]({{ site.dcv_maui_api }}utility/multi-frame-result-cross-filter.html) is the only supported implementation of the `CapturedResultFilter`.

```csharp
void AddResultFilter(ICapturedResultFilter filter);
```

**Parameters**

`[in] filter`: The filter object, of type [`CapturedResultFilter`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html). Currnetly, is must be a [`MultiFrameCrossFilter`]({{ site.dcv_maui_api }}utility/multi-frame-result-cross-filter.html) object.

## RemoveResultFilter

Removes the specified `CapturedResultFilter` object.

```csharp
void RemoveResultFilter(ICapturedResultFilter filter);
```

**Parameters**

`[in] filter`: The filter object, of type [`CapturedResultFilter`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html).
