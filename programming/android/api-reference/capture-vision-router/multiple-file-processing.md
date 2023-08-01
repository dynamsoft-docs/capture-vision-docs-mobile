---
layout: default-layout
Title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The APIs of the CaptureVisionRouter for processing multiple Images/Pages.
Keywords: capture vision, multiple-file processing, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`setInput`](#setinput) | Sets an image source to provide images for consecutive process. |
| [`getInput`](#getinput) | Gets the attached image source adapter object of the capture vision router. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Registers a ImageSourceStateListener to get callback when the status of ImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes a ImageSourceStateListener. |
| [`addResultReceiver`](#addresultreceiver) | Registers a CapturedResultReceiver to get callback when CapturedResult output. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes a CapturedResultReceiver. |
| [`startCapturing`](#startcapturing) | Start capturing with the targeting template. |
| [`stopCapturing`](#stopcapturing) | Stop capturing. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Registers a CaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Removes a CaptureStateListener. |
| [`addResultFilter`](#addresultfilter) | Registers a CapturedResultFilter to get callback when filtered result output. |
| [`removeResultFilter`](#removeresultfilter) | Removes a CapturedResultFilter. |

## setInput

Sets an image source to provide images for consecutive process.

```java
void setInput(ImageSourceAdapter adapter) throws CaptureVisionRouterException;
```

**Parameters**

`[in] adapter`: An object of [`ImageSourceAdapter`](../core/basic-structures/image-source-adapter.md). You can use a internally implemented [`ImageSourceAdapter`](../core/basic-structures/image-source-adapter.md) such as `CameraEnhancer`, `DirectoryFetcher` and `FileFetcher`.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## getInput

Gets the attached image source adapter object of the capture vision router.

```java
ImageSourceAdapter getInput();
```

**Return Value**

The attached image source adapter object of the capture vision router.

## addImageSourceStateListener

Register a [`ImageSourceStateListener`](./auxiliary-classes/image-source-state-listener.md) to get callback when the status of [`ImageSourceAdapter`](../core/basic-structures/image-source-adapter.md) received.

```java
void addImageSourceStateListener(ImageSourceStatestener listener) throws CaptureVisionRouterException;
```

**Parameters**

`[in] listener`: An object of [`ImageSourceStateListener`](./auxiliary-classes/image-source-state-listener.md).

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeImageSourceStateListener

Removes a [`ImageSourceStateListener`](./auxiliary-classes/image-source-state-listener.md).

```java
void removeImageSourceStateListener(ImageSourceStateListener listener) throws CaptureVisionRouterException;
```

**Parameters**

`[in] listener`: An object of [`ImageSourceStateListener`](./auxiliary-classes/image-source-state-listener.md).

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## addResultReceiver

Register a [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) to get callback when `CapturedResult` output.

```java
void addResultReceiver(CapturedResultReceiver receiver) throws CaptureVisionRouterException;
```

**Parameters**

`[in] receiver`: An object of [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeResultReceiver

Removes a [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) .

```java
void removeResultReceiver(CapturedResultReceiver receiver) throws CaptureVisionRouterException;
```

**Parameters**

`[in] receiver`: An object of [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## startCapturing

Start capturing with the targeting template.

```java
void startCapturing(String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`[in] templateName`: The name of a template that you have previously set via `initSettings` or `initSettingsFromFile`.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* Your templateName is invalid.
* Your image source is invalid.

## stopCapturing

Stop capturing.

```java
void stopCapturing();
```

## addCaptureStateListener

Register a [`CaptureStateListener`](./auxiliary-classes/capture-state-listener.md) to get callback when capture state changes.

```java
void addCaptureStateListener(CaptureStateListener listener) throws CaptureVisionRouterException;
```

**Parameters**

`[in] listener`: A delegate object of [`CaptureStateListener`](./auxiliary-classes/capture-state-listener.md) to receive the capture state.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeCaptureStateListener

Removes a [`CaptureStateListener`](./auxiliary-classes/capture-state-listener.md).

```java
void removeCaptureStateListener(CaptureStateListener listener) throws CaptureVisionRouterException;
```

**Parameters**

`[in] listener`: An object of [`CaptureStateListener`](./auxiliary-classes/capture-state-listener.md)

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## addResultFilter

Register a [`CapturedResultFilter`](../core/basic-structures/captured-result-filter.md) to get callback when filtered result output.

```java
void addResultFilter(CapturedResultFilter filter) throws CaptureVisionRouterException;
```

**Parameters**

`[in] filter`: An object of [`CapturedResultFilter`](../core/basic-structures/captured-result-filter.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeResultFilter

Removes a [`CapturedResultFilter`](../core/basic-structures/captured-result-filter.md) .

```java
void removeResultFilter(CapturedResultFilter filter) throws CaptureVisionRouterException;
```

**Parameters**

`[in] filter`: An object of [`CapturedResultFilter`](../core/basic-structures/captured-result-filter.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.
