---
layout: default-layout
title: DSCaptureVisionRouter - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSCaptureVisionRouter of Dynamsoft Capture Vision Router Module is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain Final results or Intermediate Results.
keywords: CaptureVisionRouter index, cvr, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCaptureVisionRouter

The `DSCaptureVisionRouter` class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain Final results or Intermediate Results.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCaptureVisionRouter : NSObject
```
2. 
```swift
class CaptureVisionRouter : NSObject
```

## Constructor

| Method | Description |
| ------ | ----------- |
| [`init`](constructors.md#init) | Creates an instance of `CaptureVisionRouter`. |

## Single-File Processing

| Method | Description |
| ------ | ----------- |
| [`captureFromFile`](single-file-processing.md#capturefromfile) | Processes an image file to derive important information. |
| [`captureFromFileBytes`](single-file-processing.md#capturefromfilebytes) | Processes an image file in memory to derive important information. |
| [`captureFromBuffer`](single-file-processing.md#capturefrombuffer) | Processes an `ImageData` object to derive important information. |
| [`captureFromImage`](single-file-processing.md#capturefromimage) | Processes an `UIImage` to derive important information. |

## Multiple-File Processing

| Method | Description |
| ------ | ----------- |
| [`setInput`](multiple-file-processing.md#setinput) | Sets up an image source to provide images for continuous processing. |
| [`getInput`](multiple-file-processing.md#getinput) | Returns the image source object. |
| [`addImageSourceStateListener`](multiple-file-processing.md#addimagesourcestatelistener) | Registers a DSImageSourceStateListener to get callback when the status of DSImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](multiple-file-processing.md#removeimagesourcestatelistener) | Removes a DSImageSourceStateListener. |
| [`removeAllImageSourceStateListeners`](#removeallimagesourcestatelisteners) | Removes all user-added [`ImageSourceStateListeners`](auxiliary-classes/image-source-state-listener.html). |
| [`addResultReceiver`](multiple-file-processing.md#addresultreceiver) | Registers a DSCapturedResultReceiver to get callback when DSCapturedResult output. |
| [`removeResultReceiver`](multiple-file-processing.md#removeresultreceiver) | Removes a DSCapturedResultReceiver. |
| [`removeAllResultReceivers`](#removeallresultreceivers) | Removes all user-added [`CapturedResultReceivers`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html). |
| [`startCapturing`](multiple-file-processing.md#startcapturing) | Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source. |
| [`stopCapturing`](multiple-file-processing.md#stopcapturing) | Stops the capturing process. |
| [`pauseCapturing`](multiple-file-processing.md#pausecapturing) | Pauses the Capture Vision Router. |
| [`resumeCapturing`](multiple-file-processing.md#resumecapturing) | Resumes the Capture Vision Router. |
| [`addCaptureStateListener`](multiple-file-processing.md#addcapturestatelistener) | Registers a DSCaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](multiple-file-processing.md#removecapturestatelistener) | Removes a DSCaptureStateListener. |
| [`removeAllCaptureStateListeners`](#removeallcapturestatelisteners) | Removes all user-added [`CaptureStateListeners`](auxiliary-classes/capture-state-listener.html). |
| [`addResultFilter`](multiple-file-processing.md#addresultfilter) | Adds a `CaptureResultFilter` object to filter non-essential results. |
| [`removeResultFilter`](multiple-file-processing.md#removeresultfilter) | Removes the specified `CaptureResultFilter` object. |
| [`removeAllResultFilters`](#removeallresultfilters) | Removes all user-added `CapturedResultFilters`. |
| [`switchCapturingTemplate`](multiple-file-processing.md#switchcapturingtemplate) | Switch the image processing settings with the CaptureVisionTemplate name during the image processing workflow. |

## Settings

| Method | Description |
| ------ | ----------- |
| [`initSettings`](settings.md#initsettings) | Initialize the Capture Vision settings with a JSON String. |
| [`initSettingsFromFile`](settings.md#initsettingsfromfile) | Initialize the Capture Vision settings with a JSON file. |
| [`getSimplifiedSettings`](settings.md#getsimplifiedsettings) | Retrieves a simplified version of the Capture Vision settings for a specific template. |
| [`updateSettings`](settings.md#updatesettings) | Update Capture Vision settings with an object of `DSSimplifiedCaptureVisionSettings`. |
| [`resetSettings`](settings.md#resetsettings) | Resets all templates to factory settings. |
| [`outputSettings`](settings.md#outputsettings) | Output the targeting Capture Vision settings to a JSON string. |
| [`outputSettingsToFile`](settings.md#outputsettingstofile) | Output the targeting Capture Vision settings to a JSON file. |
| [`clearDLModelBuffers`](settings.md#cleardlmodelbuffers) | Clear the buffered deep learning models to release the memory. |
| [`setGlobalIntraOpNumThreads`](settings.md#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |
| [`getTemplateNames`](#gettemplatenames) | Retrieves the names of all the currently available templates. |

## Intermediate Result

| Method | Description |
| ------ | ----------- |
|  [`getIntermediateResultManager`](intermediate-result.md#getintermediateresultmanager) | Gets the object of `IntermediateResultManager`. |

## Buffered Items

| Method | Description |
| ------ | ----------- |
|  [`getBufferedItemsManager`](buffered-items.md#getbuffereditemsmanager) | Gets the object of `BufferedItemsManager`. |
