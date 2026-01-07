---
layout: default-layout
title: Processing multiple Images/Pages - Dynamsoft Capture Vision Android Edition API Reference
description: The multiple Images/Pages processing APIs of the CaptureVisionRouter class for DCV Android Edition.
keywords: capture vision, multiple-file processing, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`setInput`](#setinput) | Sets up an image source to provide images for continuous processing. |
| [`getInput`](#getinput) | Returns the image source object. |
| [`addResultReceiver`](#addresultreceiver) | Adds a [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object as the receiver of captured results. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes the specified [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object. |
| [`removeAllResultReceivers`](#removeallresultreceivers) | Removes all user-added [`CapturedResultReceivers`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html). |
| [`startCapturing`](#startcapturing) | Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source. |
| [`stopCapturing`](#stopcapturing) | Stops the capturing process. |
| [`pauseCapturing`](#pausecapturing) | Pauses the Capture Vision Router. |
| [`resumeCapturing`](#resumecapturing) | Resumes the Capture Vision Router. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Registers a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) to be used as a callback when capture state is received. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Removes a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) that has been configured for the Capture Vision Router. |
| [`removeAllCaptureStateListeners`](#removeallcapturestatelisteners) | Removes all user-added [`CaptureStateListeners`](auxiliary-classes/capture-state-listener.html). |
| [`addResultFilter`](#addresultfilter) | Adds a `CapturedResultFilter` object to filter non-essential results. |
| [`removeResultFilter`](#removeresultfilter) | Removes the specified `CapturedResultFilter` object. |
| [`removeAllResultFilters`](#removeallresultfilters) | Removes all user-added `CapturedResultFilters`. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Register a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) to get callback when the status of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) received. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) from the Capture Vision Router. |
| [`removeAllImageSourceStateListeners`](#removeallimagesourcestatelisteners) | Removes all user-added [`ImageSourceStateListeners`](auxiliary-classes/image-source-state-listener.html). |
| [`switchCapturingTemplate`](#switchcapturingtemplate) | Switch the image processing settings with the CaptureVisionTemplate name during the image processing workflow. |

## setInput

Sets up an image source to provide images for continuous processing.

```java
void setInput(ImageSourceAdapter imageSourceAdapter) throws CaptureVisionRouterException;
```

**Parameters**

`[in] imageSourceAdapter`: An object of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html).

You can use the following officially implemented `ImageSourceAdapter` classes:

- [`CameraEnhancer`]({{ site.dce_android_api }}primary-api/camera-enhancer.html): A camera class that can capture video frames continuously.
- [`DirectoryFetcher`]({{ site.dcv_android_api }}utility/directory-fetcher.html): A class that can fetch all images from a directory. It supports the multi-page files like .PDF and .TIFF.
- [`FileFetcher`]({{ site.dcv_android_api }}utility/file-fetcher.html): A class that can fetch the specified image(s). It supports the multi-page files like .PDF and .TIFF.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## getInput

Returns the image source object.

```java
ImageSourceAdapter getInput();
```

**Return Value**

The `ImageSourceAdapter` object that is bind with this `CaptureVisionRouter` object.

## addResultReceiver

Adds a [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object as the receiver of captured results.

```java
void addResultReceiver(CapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: The receiver object, of type [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

## removeResultReceiver

Removes the specified [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object.

```java
void removeResultReceiver(CapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: The receiver object, of type [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

## removeAllResultReceivers

Removes all user-added [`CapturedResultReceivers`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

```java
void removeAllResultReceivers();
```

## startCapturing

Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source.

```java
void startCapturing(String templateName, CompletionListener completionHandler);
```

**Parameters**

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_android_api }}capture-vision-router/enum/preset-template.html?lang=android) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
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

Adds a `CapturedResultFilter` object to filter non-essential results. Currnetly, [`MultiFrameCrossFilter`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html) is the only supported implementation of the `CapturedResultFilter`.

```java
void addResultFilter(CapturedResultFilter filter);
```

**Parameters**

`[in] filter`: The filter object, of type [`CapturedResultFilter`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html). Currnetly, is must be a [`MultiFrameCrossFilter`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html) object.

## removeResultFilter

Removes the specified `CapturedResultFilter` object.

```java
void removeResultFilter(CapturedResultFilter filter);
```

**Parameters**

`[in] filter`: The filter object, of type [`CapturedResultFilter`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html).

## removeResultFilter

Removes all user-added`CapturedResultFilters`.

```java
void removeAllResultFilters();
```

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

## removeAllCaptureStateListeners

Removes all user-added [`CaptureStateListeners`](auxiliary-classes/capture-state-listener.html).

```java
void removeAllCaptureStateListeners();
```

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

## removeAllImageSourceStateListeners

Removes all user-added [`ImageSourceStateListeners`](auxiliary-classes/image-source-state-listener.html).

```java
void removeAllImageSourceStateListeners();
```

## switchCapturingTemplate

Switch the image processing settings with the CaptureVisionTemplate name during the image processing workflow.

```java
void switchCapturingTemplate(String templateName) throws CaptureVisionException;
```

**Parameters**

`[in] templateName`: The name of the new capturing template to apply.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
