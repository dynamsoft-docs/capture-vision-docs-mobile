---
layout: default-layout
Title: CaptureVisionRouter - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class CaptureVisionRouter of Dynamsoft Capture Vision Router Module is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain Final results or Intermediate Results.
Keywords: capture vision router, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CaptureVisionRouter

The `CaptureVisionRouter` class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Final results]({{site.architecture}}output.html#final-results?lang=android) or [Intermediate Results]({{site.architecture}}output.html#intermediate-results?lang=android).

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
class CaptureVisionRouter
```

## Constructor

| Method                                                           | Description                                           |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| [`CaptureVisionRouter`](constructors.md#ccapturevisionrouter)    | Default constructor of `CaptureVisionRouter` object. |

## Single-File Processing

| Method                                       | Description                                               |
| ---------------------------------------------- | --------------------------------------------------------- |
| [`capture(filePath,templateName)`](single-file-processing.md#capturefilepathtemplatename) | Capture data from the file specified by the file path. |
| [`capture(fileBytes,templateName)`](single-file-processing.md#capturefilebytestemplatename) | Capture data from a given file in memory. |
| [`capture(imageData,templateName)`](single-file-processing.md#captureimagedatatemplatename) | Capture data from the memory buffer via a [`ImageData`](../core/basic-structures/image-data.md) object. |
| [`capture(bitmap,templateName)`](single-file-processing.md#capturebitmaptemplatename) | Capture data from the given Bitmap. |

## Multiple-File Processing

| Method | Description |
| ------ | ----------- |
| [`setInput`](multiple-file-processing.md#setinput) | Sets an image source to provide images for consecutive process. |
| [`getInput`](multiple-file-processing.md#getinput) | Gets the attached image source adapter object of the capture vision router. |
| [`addImageSourceStateListener`](multiple-file-processing.md#addimagesourcestatelistener) | Register a ImageSourceStateListener to get callback when the status of ImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](multiple-file-processing.md#removeimagesourcestatelistener) | Removes a ImageSourceStateListener. |
| [`addResultReceiver`](multiple-file-processing.md#addresultreceiver) | Register a CapturedResultReceiver to get callback when CapturedResult output. |
| [`removeResultReceiver`](multiple-file-processing.md#removeresultreceiver) | Removes a CapturedResultReceiver. |
| [`startCapturing`](multiple-file-processing.md#startcapturing) | Start capturing with the targeting template. |
| [`stopCapturing`](multiple-file-processing.md#stopcapturing) | Stop capturing. |
| [`addCaptureStateListener`](multiple-file-processing.md#addcapturestatelistener) | Register a CaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](multiple-file-processing.md#removecapturestatelistener) | Removes a CaptureStateListener. |
| [`addResultFilter`](multiple-file-processing.md#addresultfilter) | Register a CapturedResultFilter to get callback when filtered result output. |
| [`removeResultFilter`](multiple-file-processing.md#removeresultfilter) | Removes a CapturedResultFilter. |

## Settings

| Method | Description |
| ------ | ----------- |
| [`initSettings`](settings.md#initsettings) | Initialize the Capture Vision settings with a JSON String. |
| [`initSettingsFromFile`](settings.md#initsettingsfromfile) | Initialize the Capture Vision settings with a JSON file. |
| [`getSimplifiedSettings`](settings.md#getsimplifiedsettings) | Retrieves a simplified version of the Capture Vision settings for a specific template. |
| [`updateSettings`](settings.md#updatesettings) | Update Capture Vision settings with an object of `SimplifiedCaptureVisionSettings`. |
| [`resetSettings`](settings.md#resetsettings) | Resets all templates to factory settings. |
| [`outputSettings`](settings.md#outputsettings) | Output the targeting Capture Vision settings to a JSON string. |
| [`outputSettingsToFile`](settings.md#outputsettingstofile) | Output the targeting Capture Vision settings to a JSON file. |

## Intermediate Result

| Method | Description |
| ------ | ----------- |
|  [`getIntermediateResultManager`](intermediate-result.md#getintermediateresultmanager) | Gets the object of `IntermediateResultManager`. |
