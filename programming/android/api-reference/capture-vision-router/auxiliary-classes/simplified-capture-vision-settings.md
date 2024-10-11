---
layout: default-layout
title: SimplifiedCaptureVisionSettings - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class SimplifiedCaptureVisionSettings of Dynamsoft Capture Vision Router Module contains settings for capturing and recognizing images with the CaptureVisionRouter class.
keywords: Capture Vision settings, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` class contains settings for capturing and recognizing images with the `CaptureVisionRouter` class.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
class SimplifiedCaptureVisionSettings
```

## Methods & Attributes

| Method               | Description |
|----------------------|-------------|
| [`toJSON`](#tojson) | Generate the current `SimplifiedCaptureVisionSettings` object to a JSON string. |
| [`fromJSON`](#fromjson) | Generate a `SimplifiedCaptureVisionSettings` object from a JSON string. |

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`capturedResultItemTypes`](#capturedresultitemtypes) | *int* | Specifies the type(s) of CapturedItem(s) that will be captured. |
| [`roi`](#roi) | *[Quadrilateral](../../core/basic-structures/quadrilateral.md)* | Specifies the region of interest (ROI) where the image capture and recognition will take place. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *boolean* | Specifies whether the ROI is measured in pixels or as a percentage of the image size. |
| [`maxParallelTasks`](#maxparalleltasks) | *int* | Specifies the maximum number of parallel tasks that can be used for image capture and recognition. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *int* | Set the minimum capture interval. It is measured in millisecond. |
| [`timeout`](#timeout) | *int* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |
| [`barcodeSettings`](#barcodesettings) | *[SimplifiedBarcodeReaderSettings]({{ site.dbr_android_api }}simplified-barcode-reader-settings.html) \** | Specifies the settings for `DynamsoftBarcodeReader` tasks. |
| [`labelSettings`](#labelsettings) | *[SimplifiedLabelRecognizerSettings]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html) \** | Specifies the settings for `DynamsoftLabelRecognizer` tasks. |
| [`documentSettings`](#documentsettings) | *[SimplifiedDocumentNormalizerSettings]({{ site.ddn_android_api }}simplified-document-normalizer-settings.html) \** | Specifies the settings for `DynamsoftDocumentNormalizer` tasks. |

### toJSON

Transform the current `SimplifiedLabelRecognizerSettings` object to a JSON string.

```java
String toJSON();
```

**Return Value**

The string that generated from the current `SimplifiedLabelRecognizerSettings` object.

### fromJSON

Generate a `SimplifiedLabelRecognizerSettings` object from a JSON string.

```java
static SimplifiedLabelRecognizerSettings fromJSON(String jsonString);
```

**Return Value**

The generated `SimplifiedLabelRecognizerSettings` object.

### capturedResultItemTypes

Specifies the type(s) of CapturedItem(s) that will be captured.

```java
@EnumCapturedResultItemType
int capturedResultItemTypes;
```

You can specify multiple types. For example, you can use the following code to add `CRIT_ORIGINAL_IMAGE` to the captured results of `PT_READ_BARCODES` template.

```java
try {
    SimplifiedCaptureVisionSettings settings = cvr.getSimplifiedSettings(EnumPresetTemplate.PT_READ_BARCODES);
    settings.capturedResultItemTypes = EnumCapturedResultItemType.CRIT_BARCODE | EnumCapturedResultItemType.CRIT_ORIGINAL_IMAGE;
    cvr.updateSettings(EnumPresetTemplate.PT_READ_BARCODES, settings);
} catch (CaptureVisionRouterException e) {
    throw new RuntimeException(e);
}
```

> View [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android) about all supported result item types.

### roi

Specifies the region of interest (ROI) where the image capture and recognition will take place.

```java
Quadrilateral roi;
```

### roiMeasuredInPercentage

Specifies whether the ROI is measured in pixels or as a percentage of the image size.

```java
boolean roiMeasuredInPercentage;
```

### maxParallelTasks

Specifies the maximum number of parallel tasks that can be used for image capture and recognition.

```java
int maxParallelTasks;
```

### minImageCaptureInterval

Set the minimum capture interval. It is measured in millisecond.

```java
int minImageCaptureInterval;
```

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

```java
int timeout;
```

### barcodeSettings

Specifies the settings for `DynamsoftBarcodeReader` tasks with a [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_android_api }}simplified-barcode-reader-settings.html) object.

```java
SimplifiedBarcodeReaderSettings barcodeSettings;
```

### labelSettings

Specifies the settings for `DynamsoftLabelRecognizer` tasks with a [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html) object.

```java
SimplifiedLabelRecognizerSettings labelSettings;
```

### documentSettings

Specifies the settings for `DynamsoftDocumentNormalizer` tasks with a [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_android_api }}simplified-document-normalizer-settings.html) object.

```java
SimplifiedDocumentNormalizerSettings documentSettings;
```
