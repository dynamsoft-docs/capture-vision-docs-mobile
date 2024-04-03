---
layout: default-layout
title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The multiple Images/Pages processing APIs of the CaptureVisionRouter class for DCV Android Edition.
keywords: capture vision, multiple-file processing, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`setInput`](#setinput) | Sets an image source that will provide images to be consecutively processed. |
| [`getInput`](#getinput) | Gets the attached image source adapter object of the Capture Vision Router. |
| [`addResultReceiver`](#addresultreceiver) | Registers a [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be used as a callback when the library outputs a [`CapturedResult`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result.html). |
| [`removeResultReceiver`](#removeresultreceiver) | Removes a [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) from the Capture Vision Router. |
| [`startCapturing`](#startcapturing) | Start capturing with the specified template. |
| [`stopCapturing`](#stopcapturing) | Tells the Capture Vision Router to stop capturing. |
| [`pauseCapturing`](#pausecapturing) | Pauses the Capture Vision Router. |
| [`resumeCapturing`](#resumecapturing) | Resumes the Capture Vision Router. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Registers a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) to be used as a callback when capture state is received. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Removes a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) that has been configured for the Capture Vision Router. |
| [`addResultFilter`](#addresultfilter) | Registers a `CapturedResultFilter` to be used as a callback to filter the `CapturedResult`. |
| [`removeResultFilter`](#removeresultfilter) | Removes a `CapturedResultFilter` that has been configured for the Capture Vision Router. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Register a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) to get callback when the status of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) received. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) from the Capture Vision Router. |

## setInput

Sets up an image source with an `ImageSourceAdapter` object for continuous processing. The `CaptureVisionRputer` will consecutively retrieve images from the `ImageSourceAdapter` after you start the capturing.

```java
void setInput(ImageSourceAdapter adapter) throws CaptureVisionRouterException;
```

**Parameters**

`[in] adapter`: An object of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html).

You can use the following officially implemented `ImageSourceAdapter` classes:

- [`CameraEnhancer`]({{ site.dce_android_api }}primary-api/camera-enhancer.html): A camera class that can capture video frames continuously.
- [`DirectoryFetcher`]({{ site.dcv_android_api }}utility/directory-fetcher.html): A class that can fetch all images from a directory. It supports the multi-page files like .PDF and .TIFF.
- [`FileFetcher`]({{ site.dcv_android_api }}utility/file-fetcher.html): A class that can fetch the specified image(s). It supports the multi-page files like .PDF and .TIFF.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## getInput

Gets the `ImageSourceAdapter` object that is bind with this `CaptureVisionRouter` object.

```java
ImageSourceAdapter getInput();
```

**Return Value**

The `ImageSourceAdapter` object that is bind with this `CaptureVisionRouter` object.

## addResultReceiver

Registers a [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) to be used as a callback when an image is processed.

```java
void addResultReceiver(CapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: The receiver object, of type [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

## removeResultReceiver

Removes the specified [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object from the Capture Vision Router.

```java
void removeResultReceiver(CapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: The receiver object, of type [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

## startCapturing

Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source.

```java
void startCapturing(String templateName, CompletionListener completionHandler);
```

**Parameters**

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?lang=android) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

`[in] completionHandler`: A [`CompletionListener`]({{ site.dcv_android_api }}core/basic-structures/completion-listener.html) the system calls after it finishes the startCapturing.

## stopCapturing

Stops the capturing process.

```java
void stopCapturing();
```

## pauseCapturing

Pauses the capturing.

```java
void pauseCapturing();
```

## resumeCapturing

Resumes the capturing.

```java
void resumeCapturing();
```

## addResultFilter

Adds a [`CapturedResultFilter`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) object to filter the `CapturedResult`. Currnetly, [`MultiFrameCrossFilter`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html) is the only supported implementation of the `CapturedResultFilter`.

```java
void addResultFilter(CapturedResultFilter filter);
```

**Parameters**

`[in] filter`: The filter object, of type [`CapturedResultFilter`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html). Currnetly, is must be a [`MultiFrameCrossFilter`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html) object.

## removeResultFilter

Removes the specified `CapturedResultFilter` that has been configured for the Capture Vision Router.

```java
void removeResultFilter(CapturedResultFilter filter);
```

**Parameters**

`[in] filter`: The filter object, of type [`CapturedResultFilter`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html).

## addCaptureStateListener

Registers a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) to be used as a callback when capture state is received.

```java
void addCaptureStateListener(CaptureStateListener listener);
```

**Parameters**

`[in] listener`: A delegate object of [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) to receive the capture state.

## removeCaptureStateListener

Removes a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) that has been configured for the Capture Vision Router.

```java
void removeCaptureStateListener(CaptureStateListener listener);
```

**Parameters**

`[in] listener`: An object of [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html)

## addImageSourceStateListener

Register a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) to get callback when the status of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) received.

```java
void addImageSourceStateListener(ImageSourceStatestener listener);
```

**Parameters**

`[in] listener`: An object of [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html).

## removeImageSourceStateListener

Removes a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) from the Capture Vision Router.

```java
void removeImageSourceStateListener(ImageSourceStateListener listener);
```

**Parameters**

`[in] listener`: An object of [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html).
