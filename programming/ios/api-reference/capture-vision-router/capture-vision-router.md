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

*Assembly:* DynamsoftCore.framework

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
| [`captureFromFile`](single-file-processing.md#capturefromfile) | Capture data from the file specified by the file path. |
| [`captureFromFileBytes`](single-file-processing.md#capturefromfilebytes) | Capture data from a given file in memory. |
| [`captureFromBuffer`](single-file-processing.md#capturefrombuffer) | Capture data from the memory buffer via a `DSImageData` object. |
| [`captureFromImage`](single-file-processing.md#capturefromimage) | Capture data from the given image. |


## Multiple-File Processing

| Method | Description |
| ------ | ----------- |
| [`setInput`](multiple-file-processing.md#setinput) | Sets an image source to provide images for consecutive process. |
| [`getInput`](multiple-file-processing.md#getinput) | Gets the attached image source adapter object of the capture vision router. |
| [`addImageSourceStateListener`](multiple-file-processing.md#addimagesourcestatelistener) | Registers a DSImageSourceStateListener to get callback when the status of DSImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](multiple-file-processing.md#removeimagesourcestatelistener) | Removes a DSImageSourceStateListener. |
| [`addResultReceiver`](multiple-file-processing.md#addresultreceiver) | Registers a DSCapturedResultReceiver to get callback when DSCapturedResult output. |
| [`removeResultReceiver`](multiple-file-processing.md#removeresultreceiver) | Removes a DSCapturedResultReceiver. |
| [`startCapturing`](multiple-file-processing.md#startcapturing) | Start capturing with the targeting template. |
| [`stopCapturing`](multiple-file-processing.md#stopcapturing) | Start capturing with the targeting template. |
| [`pauseCapturing`](multiple-file-processing.md#pausecapturing) | Pauses the Capture Vision Router. |
| [`resumeCapturing`](multiple-file-processing.md#resumecapturing) | Resumes the Capture Vision Router. |
| [`addCaptureStateListener`](multiple-file-processing.md#addcapturestatelistener) | Registers a DSCaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](multiple-file-processing.md#removecapturestatelistener) | Removes a DSCaptureStateListener. |
| [`addResultFilter`](multiple-file-processing.md#addresultfilter) | Registers a DSCapturedResultFilter to get callback when filtered result output. |
| [`removeResultFilter`](multiple-file-processing.md#removeresultfilter) | Removes a DSCapturedResultFilter. |

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

## Intermediate Result

| Method | Description |
| ------ | ----------- |
|  [`getIntermediateResultManager`](intermediate-result.md#getintermediateresultmanager) | Gets the object of `IntermediateResultManager`. |
