---
layout: default-layout
title: SimplifiedCaptureVisionSettings Class - Dynamsoft Capture Vision Flutter
description: SimplifiedCaptureVisionSettings class of DCV Flutter edition provides settings for capturing and recognizing images with the CaptureVisionRouter class.
keywords: roi, result item type, min interval, timeout, flutter, settings, foundational
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` class contains the general settings for all of the Capture Vision functional products (Barcode Reader, Label Recognizer, Document Normalizer, Code Parser). These settings can help for capturing and recognizing images with the `CaptureVisionRouter` class.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class SimplifiedCaptureVisionSettings
```

## Properties

| Property | Type | Description |
| ---------- | ---- | ----------- |
| [`roi`](#roi) | *Quadrilateral* | Sets the region of interest (ROI) when reading from a camera or a static image. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *bool* | Establishes whether the ROI is measured in pixels or as a percentage of the image/frame size. |
| [`maxParallelTasks`](#maxparalleltasks) | *int* | Determines the maximum number of parallel tasks allowed for image capture and recognition. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *int* | Sets the minimum interval (in milliseconds) between image captures. |
| [`timeout`](#timeout) | *int* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |
| [`barcodeSettings`](#barcodesettings) | *[SimplifiedBarcodeReaderSettings]({{ site.dbr_flutter_api }}barcode-reader/simplified-barcode-reader-settings.html)* | The settings for the `DynamsoftBarcodeReader` tasks. |
| [`labelSettings`](#labelsettings) | *[SimplifiedLabelRecognizerSettings]({{ site.dlr_flutter_api }}simplified-label-recognizer-settings.html)* | The settings for the `DynamsoftBarcodeReader` tasks. |
| [`documentSettings`](#documentsettings) | *[SimplifiedDocumentNormalizerSettings]({{ site.ddn_flutter_api }}simplified-document-normalizer-settings.html)* | The settings for the `DynamsoftBarcodeReader` tasks. |

### roi

Sets the region of interest (ROI) when reading from a camera or a static image. If the camera is being used, any scan region that is set will be represented visually on the camera view.

```dart
Quadrilateral roi;
```

### roiMeasuredInPercentage

Specifies whether the region of interest (ROI) is measured in pixels or as a percentage of the image size.

```dart
bool roiMeasuredInPercentage;
```

### maxParallelTasks

Determines the maximum number of parallel tasks allowed for image capture and recognition.

```dart
int maxParallelTasks;
```

### minImageCaptureInterval

Sets the minimum interval (in milliseconds) between image captures.

```dart
int minImageCaptureInterval;
```

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

```dart
int Timeout { get; set; }
```

### barcodeSettings

The settings for the `DynamsoftBarcodeReader` tasks as a [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_flutter_api }}barcode-reader/simplified-barcode-reader-settings.html) object.

```dart
SimplifiedBarcodeReaderSettings? barcodeSettings;
```

### labelSettings

The settings for the `DynamsoftLabelRecognizer` tasks as a [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_flutter_api }}simplified-label-recognizer-settings.html) object.

```dart
SimplifiedLabelRecognizerSettings? labelSettings;
```

### documentSettings

The settings for the `DynamsoftDocumentNormalizer` tasks as a [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_flutter_api }}simplified-document-normalizer-settings.html) object.

```dart
SimplifiedDocumentNormalizerSettings? documentSettings;
```
