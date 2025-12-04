---
layout: default-layout
title: SimplifiedCaptureVisionSettings - Dynamsoft Capture Vision React Native
description: SimplifiedCaptureVisionSettings interface of DCV React Native edition provides settings for capturing and recognizing images with the CaptureVisionRouter class.
keywords: roi, result item type, min interval, timeout, react native, settings, foundational
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# SimplifiedCaptureVisionSettings

Interface `SimplifiedCaptureVisionSettings` contains the general settings for all of the Capture Vision functional products (Barcode Reader, Label Recognizer, Document Normalizer, Code Parser). These settings can help for capturing and recognizing images with the `CaptureVisionRouter` class.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface SimplifiedCaptureVisionSettings
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`barcodeSettings`](#barcodesettings) | *[SimplifiedBarcodeReaderSettings]({{ site.dbr_react_native_api }}barcode-reader/simplified-barcode-reader-settings.html)* | The settings for the `DynamsoftBarcodeReader` tasks. |
| [`documentSettings`](#documentsettings) | *[SimplifiedDocumentNormalizerSettings]({{ site.ddn_react_native_api }}simplified-document-normalizer-settings.html)* | The settings for the `DynamsoftBarcodeReader` tasks. |
| [`labelSettings`](#labelsettings) | *[SimplifiedLabelRecognizerSettings]({{ site.dlr_react_native_api }}simplified-label-recognizer-settings.html)* | The settings for the `DynamsoftBarcodeReader` tasks. |
| [`maxParallelTasks`](#maxparalleltasks) | *number* | Determines the maximum number of parallel tasks allowed for image capture and recognition. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *number* | Sets the minimum interval (in milliseconds) between image captures. |
| [`outputOriginalImage`](#outputoriginalimage) | *boolean* | Specifies whether to output the original image. |
| [`roi`](#roi) | *Quadrilateral* | Sets the region of interest (ROI) when reading from a camera or a static image. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *boolean* | Establishes whether the ROI is measured in pixels or as a percentage of the image/frame size. |
| [`timeout`](#timeout) | *number* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |

### barcodeSettings

The settings for the `DynamsoftBarcodeReader` tasks as a [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_react_native_api }}barcode-reader/simplified-barcode-reader-settings.html) object.

```js
barcodeSettings?: SimplifiedBarcodeReaderSettings;
```

### documentSettings

The settings for the `DynamsoftDocumentNormalizer` tasks as a [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_react_native_api }}simplified-document-normalizer-settings.html) object.

```js
documentSettings?: SimplifiedDocumentNormalizerSettings;
```

### labelSettings

The settings for the `DynamsoftLabelRecognizer` tasks as a [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_react_native_api }}simplified-label-recognizer-settings.html) object.

```js
labelSettings?: SimplifiedLabelRecognizerSettings;
```

### maxParallelTasks

Determines the maximum number of parallel tasks allowed for image capture and recognition.

```js
maxParallelTasks?: number;
```

### minImageCaptureInterval

Sets the minimum interval (in milliseconds) between image captures.

```js
minImageCaptureInterval?: number;
```

### outputOriginalImage

Specifies whether to output the original image.

```js
outputOriginalImage?: boolean;
```

### roi

Sets the region of interest (ROI) when reading from a camera or a static image. If the camera is being used, any scan region that is set will be represented visually on the camera view.

```js
roi?: Quadrilateral;
```

### roiMeasuredInPercentage

Specifies whether the region of interest (ROI) is measured in pixels or as a percentage of the image size.

```js
roiMeasuredInPercentage?: boolean;
```

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

```js
timeout?: number;
```
