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
| [`setInput`](#setinput) | Sets an image source that will provide images to be consecutively processed. |
| [`getInput`](#getinput) | Gets the attached image source adapter object of the Capture Vision Router. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Register a [`ImageSourceStateListener`](../auxiliary-classes/image-source-state-listener.md) to get callback when the status of [`ImageSourceAdapter`](../core/basic-structures/image-source-adapter.md) received. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes a [`ImageSourceStateListener`](../auxiliary-classes/image-source-state-listener.md) from the Capture Vision Router. |
| [`addResultReceiver`](#addresultreceiver) | Registers a [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) to be used as a callback when the library outputs a [`CapturedResult`](../core/basic-structures/captured-result.md). |
| [`removeResultReceiver`](#removeresultreceiver) | Removes a [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) from the Capture Vision Router. |
| [`startCapturing`](#startcapturing) | Start capturing with the specified template. |
| [`stopCapturing`](#stopcapturing) | Tells the Capture Vision Router to stop capturing. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Registers a [`CaptureStateListener`](../auxiliary-classes/capture-state-listener.md) to be used as a callback when capture state is received. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Removes a [`CaptureStateListener`](../auxiliary-classes/capture-state-listener.md) that has been configured for the Capture Vision Router. |
| [`addResultFilter`](#addresultfilter) | Registers a `CapturedResultFilter` to be used as a callback to filter the `CapturedResult`. |
| [`removeResultFilter`](#removeresultfilter) | Removes a `CapturedResultFilter` that has been configured for the Capture Vision Router. |

## setInput

Sets an image source that will provide images to be consecutively processed.

```java
void setInput(ImageSourceAdapter adapter) throws CaptureVisionRouterException;
```

**Parameters**

`[in] adapter`: An object of [`ImageSourceAdapter`](../core/basic-structures/image-source-adapter.md). You can use a internally implemented [`ImageSourceAdapter`](../core/basic-structures/image-source-adapter.md) such as `CameraEnhancer`, `DirectoryFetcher` and `FileFetcher`.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## getInput

Gets the attached image source adapter object of the Capture Vision Router.

```java
ImageSourceAdapter getInput();
```

**Return Value**

The attached image source adapter object of the capture vision router.

## addImageSourceStateListener

Register a [`ImageSourceStateListener`](../auxiliary-classes/image-source-state-listener.md) to get callback when the status of [`ImageSourceAdapter`](../core/basic-structures/image-source-adapter.md) received.

```java
void addImageSourceStateListener(ImageSourceStatestener listener);
```

**Parameters**

`[in] listener`: An object of [`ImageSourceStateListener`](./auxiliary-classes/image-source-state-listener.md).

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeImageSourceStateListener

Removes a [`ImageSourceStateListener`](../auxiliary-classes/image-source-state-listener.md) from the Capture Vision Router.

```java
void removeImageSourceStateListener(ImageSourceStateListener listener);
```

**Parameters**

`[in] listener`: An object of [`ImageSourceStateListener`](../auxiliary-classes/image-source-state-listener.md).

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## addResultReceiver

Registers a [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) to be used as a callback when the library outputs a [`CapturedResult`](../core/basic-structures/captured-result.md).

```java
void addResultReceiver(CapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: An object of [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeResultReceiver

Removes a [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) from the Capture Vision Router.

```java
void removeResultReceiver(CapturedResultReceiver receiver);
```

**Parameters**

`[in] receiver`: An object of [`CapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## startCapturing

Start capturing with the specified template.

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

Tells the Capture Vision Router to stop capturing.

```java
void stopCapturing();
```

## addCaptureStateListener

Registers a [`CaptureStateListener`](../auxiliary-classes/capture-state-listener.md) to be used as a callback when capture state is received.

```java
void addCaptureStateListener(CaptureStateListener listener);
```

**Parameters**

`[in] listener`: A delegate object of [`CaptureStateListener`](../auxiliary-classes/capture-state-listener.md) to receive the capture state.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeCaptureStateListener

Removes a [`CaptureStateListener`](../auxiliary-classes/capture-state-listener.md) that has been configured for the Capture Vision Router.

```java
void removeCaptureStateListener(CaptureStateListener listener);
```

**Parameters**

`[in] listener`: An object of [`CaptureStateListener`](../auxiliary-classes/capture-state-listener.md)

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## addResultFilter

Registers a `CapturedResultFilter` to be used as a callback to filter the `CapturedResult`.

```java
void addResultFilter(CapturedResultFilter filter);
```

**Parameters**

`[in] filter`: An object of [`CapturedResultFilter`](../core/basic-structures/captured-result-filter.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeResultFilter

Removes a `CapturedResultFilter` that has been configured for the Capture Vision Router.

```java
void removeResultFilter(CapturedResultFilter filter);
```

**Parameters**

`[in] filter`: An object of [`CapturedResultFilter`](../core/basic-structures/captured-result-filter.md) .

**Exception**

An exception is thrown if the method is triggered after the capture is started.
