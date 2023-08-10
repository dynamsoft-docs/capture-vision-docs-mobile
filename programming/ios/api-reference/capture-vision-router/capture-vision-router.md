---
layout: default-layout
Title: DSCaptureVisionRouter - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The class DSCaptureVisionRouter of Dynamsoft Capture Vision Router Module is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain Final results or Intermediate Results.
Keywords: capture vision, objective-c, swift
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
| [`captureFromFile`](single-file-processing.md#capturefromfile) | Implement data capture on the given file. |
| [`captureFromFileBytes`](single-file-processing.md#capturefromfilebytes) | Implement data capture on the given file in memory. |
| [`captureFromBuffer`](single-file-processing.md#capturefrombuffer) | Implement data capture on the given image data. |
| [`captureFromImage`](single-file-processing.md#capturefromimage) | Implement data capture on the given UIImage. |

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
| [`addCaptureStateListener`](multiple-file-processing.md#addcapturestatelistener) | Registers a DSCaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](multiple-file-processing.md#removecapturestatelistener) | Removes a DSCaptureStateListener. |
| [`addResultFilter`](multiple-file-processing.md#addresultfilter) | Registers a DSCapturedResultFilter to get callback when filtered result output. |
| [`removeResultFilter`](multiple-file-processing.md#removeresultfilter) | Removes a DSCapturedResultFilter. |

## Settings

| Method | Description |
| ------ | ----------- |
| [`initSettings`](settings.md#initsettings) | Initialize the capture settings with a JSON String. |
| [`initSettingsFromFile`](settings.md#initsettingsfromfile) | Initialize the capture settings with a JSON file. |
| [`getSimplifiedSettings`](settings.md#getsimplifiedsettings) | Retrieves a simplified version of the capture settings for a specific template. |
| [`updateSettings`](settings.md#updatesettings) | Update capture vision settings with an object of `DSSimplifiedCaptureVisionSettings`. |
| [`resetSettings`](settings.md#resetsettings) | Resets all templates to factory settings. |
| [`outputSettings`](settings.md#outputsettings) | Output the targeting capture vision settings to a JSON string. |
| [`outputSettingsToFile`](settings.md#outputsettingstofile) | Output the targeting capture vision settings to a JSON file. |

## Intermediate Result

| Method | Description |
| ------ | ----------- |
|  [`getIntermediateResultManager`](intermediate-result.md#getintermediateresultmanager) | Gets the object of `IntermediateResultManager`. |
