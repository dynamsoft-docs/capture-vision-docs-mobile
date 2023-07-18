---
layout: default-layout
Title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The APIs of the CaptureVisionRouter for processing multiple Images/Pages.
Keywords: capture vision, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`setInput`](#setinput) | Sets an image source to provide images for consecutive process. |
| [`getInput`](#getinput) | Gets the attached image source adapter object of the capture vision router. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Regisiter a DSImageSourceStateListener to get callback when the status of DSImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Remove a DSImageSourceStateListener. |
| [`addResultReceiver`](#addresultreceiver) | Regisiter a CapturedResultReceiver to get callback when CapturedResult output. |
| [`removeResultReceiver`](#removeresultreceiver) | Remove a CapturedResultReceiver. |
| [`startCapturing`](#startcapturing) | Start capturing with the targeting template. |
| [`stopCapturing`](#stopcapturing) | Start capturing with the targeting template. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Regisiter a CaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Remove a CaptureStateListener. |
| [`addResultFilter`](#addresultfilter) | Regisiter a CapturedResultFilter to get callback when filtered result output. |
| [`removeResultFilter`](#removeresultfilter) | Remove a CapturedResultFilter. |

## setInput

Sets an image source to provide images for consecutive process.

```java
void setInput(ImageSourceAdapter adapter) throws CaptureVisionRouterException;
```

**Parameters**

`adapter`: An object of `DSImageSourceAdapter`. You can use a internally implemented `ImageSourceAdapter` such as `CameraEnhancer`, `DirectoryFetcher` and `FileFetcher`.

**Return Value**

A bool value that indicates whether the input is set successfully.

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

Regisiter a `DSImageSourceStateListener` to get callback when the status of `DSImageSourceAdapter` changes.

```java
void addImageSourceStateListener(ImageSourceStatestener listener) throws CaptureVisionRouterException;
```

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.

**Return Value**

A bool value that indicates whether the `DSImageSourceStateListener` is added successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeImageSourceStateListener

Remove a `DSImageSourceStateListener`.

```java
void removeImageSourceStateListener(ImageSourceStateListener listener) throws CaptureVisionRouterException;
```

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.

**Return Value**

A bool value that indicates whether the `DSImageSourceStateListener` is removed successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## addResultReceiver

Regisiter a `CapturedResultReceiver` to get callback when `CapturedResult` output.

```java
void addResultReceiver(CapturedResultReceiver receiver) throws CaptureVisionRouterException;
```

**Parameters**

`listener`: An object of `CapturedResultReceiver`.

**Return Value**

A bool value that indicates whether the result receiver is added successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeResultReceiver

Remove a `CapturedResultReceiver`.

```java
void removeResultReceiver(CapturedResultReceiver receiver) throws CaptureVisionRouterException;
```

**Parameters**

`listener`: An object of `CapturedResultReceiver`.

**Return Value**

A bool value that indicates whether the result receiver is removed successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## startCapturing

Start capturing with the targeting template.

```java
void startCapturing(String templateName) throws CaptureVisionRouterException;
```

**Parameters**

`templateName`: The name of a template that you have previously set via `initSettings` or `initSettingsFromFile`.

**Return Value**

A bool value that indicates whether the capture starts successfully.

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

Regisiter a `CaptureStateListener` to get callback when capture state changes.

```java
func addCaptureStateListener(_ listener:CaptureStateListener) throws -> BOOL
```

**Parameters**

`listener`: A delegate object of `CaptureStateListener` to receive the capture state.

**Return Value**

A BOOL value that indicates whether the capture state listener is added successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeCaptureStateListener

Remove a `CaptureStateListener`.

```java
func removeCaptureStateListener(_ listener:CaptureStateListener) throws -> BOOL
```

**Parameters**

`listener`: An object of `CaptureStateListener`.

**Return Value**

A BOOL value that indicates whether the capture state listener is removed successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## addResultFilter

Regisiter a `CapturedResultFilter` to get callback when filtered result output.

```java
void addResultFilter(CapturedResultFilter filter) throws CaptureVisionRouterException;
```

**Parameters**

`filter`: An object of `CapturedResultFilter`.

**Return Value**

A BOOL value that indicates whether the result filter is added successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.

## removeResultFilter

Remove a `CapturedResultFilter`.

```java
void removeResultFilter(CapturedResultFilter filter) throws CaptureVisionRouterException;
```

**Parameters**

`filter`: An object of `CapturedResultFilter`.

**Return Value**

A BOOL value that indicates whether the result filter is removed successfully.

**Exception**

An exception is thrown if the method is triggered after the capture is started.
