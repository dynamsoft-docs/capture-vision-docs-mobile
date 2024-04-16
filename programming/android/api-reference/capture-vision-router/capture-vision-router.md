---
layout: default-layout
title: CaptureVisionRouter - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class CaptureVisionRouter of Dynamsoft Capture Vision Router Module is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain Final results or Intermediate Results.
keywords: capture vision router, Java, Kotlin
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

| Method | Description |
| ------ | ----------- |
| [`CaptureVisionRouter`](constructors.md#ccapturevisionrouter)    | Default constructor of `CaptureVisionRouter` object. |

## Single-File Processing

| Method | Description |
| ------ | ----------- |
| [`capture(filePath,templateName)`](single-file-processing.md#capturefilepathtemplatename) | Processes an image file to derive important information. |
| [`capture(fileBytes,templateName)`](single-file-processing.md#capturefilebytestemplatename) | Processes an image file in memory to derive important information. |
| [`capture(imageData,templateName)`](single-file-processing.md#captureimagedatatemplatename) | Processes an `ImageData` object to derive important information. |
| [`capture(bitmap,templateName)`](single-file-processing.md#capturebitmaptemplatename) | Processes a `Bitmap` object to derive important information. |

## Multiple-File Processing

| Method | Description |
| ------ | ----------- |
| [`setInput`](multiple-file-processing.md#setinput) | Sets up an image source to provide images for continuous processing. |
| [`getInput`](multiple-file-processing.md#getinput) | Returns the image source object. |
| [`addImageSourceStateListener`](multiple-file-processing.md#addimagesourcestatelistener) | Registers a `ImageSourceStateListener` to get callback when the status of ImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](multiple-file-processing.md#removeimagesourcestatelistener) | Removes a `ImageSourceStateListener`. |
| [`addResultReceiver`](multiple-file-processing.md#addresultreceiver) | Registers a `CapturedResultReceiver` to get callback when CapturedResult output. |
| [`removeResultReceiver`](multiple-file-processing.md#removeresultreceiver) | Removes a `CapturedResultReceiver`. |
| [`startCapturing`](multiple-file-processing.md#startcapturing) | Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source. |
| [`stopCapturing`](multiple-file-processing.md#stopcapturing) | Stops the capturing process. |
| [`pauseCapturing`](multiple-file-processing.md#pausecapturing) | Pauses the Capture Vision Router. |
| [`resumeCapturing`](multiple-file-processing.md#resumecapturing) | Resumes the Capture Vision Router. |
| [`addCaptureStateListener`](multiple-file-processing.md#addcapturestatelistener) | Registers a `CaptureStateListener` to get callback when capture state changes. |
| [`removeCaptureStateListener`](multiple-file-processing.md#removecapturestatelistener) | Removes a `CaptureStateListener`. |
| [`addResultFilter`](multiple-file-processing.md#addresultfilter) | Adds a `CaptureResultFilter` object to filter non-essential results. |
| [`removeResultFilter`](multiple-file-processing.md#removeresultfilter) | Removes the specified `CaptureResultFilter` object. |

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
