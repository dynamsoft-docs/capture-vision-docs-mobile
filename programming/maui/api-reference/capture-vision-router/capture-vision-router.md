---
layout: default-layout
title: CaptureVisionRouter - Dynamsoft Capture Vision MAUI Edition
description: The CaptureVisionRouter class of DCV MAUI edition is what a user uses to interact with image-processing and semantic-processing products in their applications.
keywords: cvr, set input, settings, api, maui
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CaptureVisionRouter

The `CaptureVisionRouter` class is what a user uses to interact with image-processing and semantic-processing products in their applications. It provides the following essential APIs:

- Set input
- Config barcode reader settings
- Add result receiver
- Start barcode processing

## Definition

*Namespace:* Dynamsoft.CaptureVisionRouter.Maui

*Assembly:* Dynamsoft.CaptureVisionRouter.Maui

```csharp
class CaptureVisionRouter
```

## Single-File Processing

| Method | Description |
| ------ | ----------- |
| [`Capture(filePath,templateName)`](single-file-processing.md#capturefilepathtemplatename) | Processes an image file to derive important information. |

## Multiple-File Processing

| Method | Description |
| ------ | ----------- |
| [`SetInput`](multiple-file-processing.md#setinput) | Sets up an image source to provide images for continuous processing. |
| [`GetInput`](multiple-file-processing.md#getinput) | Returns the image source object. |
| [`AddResultReceiver`](multiple-file-processing.md#addresultreceiver) | Adds a `CapturedResultReceiver` object as the receiver of captured results. |
| [`RemoveResultReceiver`](multiple-file-processing.md#removeresultreceiver) | Removes the specified CapturedResultReceiver object. |
| [`StartCapturing`](multiple-file-processing.md#startcapturing) | Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source. |
| [`StopCapturing`](multiple-file-processing.md#stopcapturing) | Stops the capturing process. |
| [`AddResultFilter`](multiple-file-processing.md#addresultfilter) | Adds a `CaptureResultFilter` object to filter non-essential results. |
| [`RemoveResultFilter`](multiple-file-processing.md#removeresultfilter) | Removes the specified `CaptureResultFilter` object. |

## Settings

| Method | Description |
| ------ | ----------- |
| [`InitSettings`](settings.md#initsettings) | Initialize the Capture Vision settings with a JSON String. |
| [`InitSettingsFromFile`](settings.md#initsettingsfromfile) | Initialize the Capture Vision settings with a JSON file. |
| [`GetSimplifiedSettings`](settings.md#getsimplifiedsettings) | Retrieves a simplified version of the Capture Vision settings for a specific template. |
| [`UpdateSettings`](settings.md#updatesettings) | Update Capture Vision settings with an object of `SimplifiedCaptureVisionSettings`. |
| [`ResetSettings`](settings.md#resetsettings) | Resets all templates to factory settings. |
| [`OutputSettings`](settings.md#outputsettings) | Output the targeting Capture Vision settings to a JSON string. |
| [`OutputSettingsToFile`](settings.md#outputsettingstofile) | Output the targeting Capture Vision settings to a JSON file. |

## Intermediate Result

| Method | Description |
| ------ | ----------- |
| [`GetIntermediateResultManager`](intermediate-result.md#getintermediateresultmanager) | Returns an object, of type [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md), that manages intermediate results.  |
