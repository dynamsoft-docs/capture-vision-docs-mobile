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
| [`roi`](#roi) | *[Quadrilateral](../../core/basic-structures/quadrilateral.md)* | Specifies the region of interest (ROI) of the image or frame where the capture and recognition will take place. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *boolean* | Specifies whether the ROI is measured in pixels (false) or as a percentage of the image dimensions (true). |
| [`maxParallelTasks`](#maxparalleltasks) | *int* | Specifies the maximum number of parallel tasks that can be used for image capture and recognition. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *int* | Set the minimum capture interval, measured in milliseconds. |
| [`timeout`](#timeout) | *int* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |
| [`barcodeSettings`](#barcodesettings) | *[SimplifiedBarcodeReaderSettings]({{ site.dbr_android_api }}simplified-barcode-reader-settings.html)* | Specifies the settings for the `DynamsoftBarcodeReader` task. |
| [`labelSettings`](#labelsettings) | *[SimplifiedLabelRecognizerSettings]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html)* | Specifies the settings for the `DynamsoftLabelRecognizer` task. |
| [`documentSettings`](#documentsettings) | *[SimplifiedDocumentNormalizerSettings]({{ site.ddn_android_api }}simplified-document-normalizer-settings.html)* | Specifies the settings for the `DynamsoftDocumentNormalizer` task. |

### toJSON

Transform the current `SimplifiedCaptureVisionSettings` object to a JSON string.

```java
String toJSON();
```

**Return Value**

The JSON string format of the current `SimplifiedCaptureVisionSettings` object.

### fromJSON

Generate a `SimplifiedCaptureVisionSettings` object from a JSON string.

```java
static SimplifiedCaptureVisionSettings fromJSON(String jsonString);
```

**Return Value**

The generated `SimplifiedCaptureVisionSettings` object.

### capturedResultItemTypes

Specifies the type(s) of CapturedItem(s) that will be returned by the Capture Vision Router.

```java
@EnumCapturedResultItemType
int capturedResultItemTypes;
```

**Remarks**

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

> View [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android) to learn of all supported result item types.

### roi

Specifies the region of interest (ROI) of the image or frame where the capture and recognition will take place.

```java
Quadrilateral roi;
```

### roiMeasuredInPercentage

Specifies whether the ROI is measured in pixels (false) or as a percentage of the image dimensions (true).

```java
boolean roiMeasuredInPercentage;
```

### maxParallelTasks

Specifies the maximum number of parallel tasks that can be used for image capture and recognition.

```java
int maxParallelTasks;
```

### minImageCaptureInterval

Set the minimum capture interval (in milliseconds) between consecutive frames when capturing via video. In other words, it is a measure of the frequency in which frames are fetched.

```java
int minImageCaptureInterval;
```

**Remarks**

If you find that the battery consumption when using any of the Dynamsoft Capture Vision products, we recommend setting this parameter to a higher value. Please see this [article]({{ site.dbr_android }}faq/reduce-battery-consumption.html) for more info on how to reduce battery consumption.

### timeout

Specifies the maximum time (in milliseconds) allowed for image capture and recognition.

```java
int timeout;
```

### barcodeSettings

Specifies the settings for the `DynamsoftBarcodeReader` task with a [`SimplifiedBarcodeReaderSettings`]({{ site.dbr_android_api }}simplified-barcode-reader-settings.html) object.

```java
SimplifiedBarcodeReaderSettings barcodeSettings;
```

### labelSettings

Specifies the settings for the `DynamsoftLabelRecognizer` task with a [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html) object.

```java
SimplifiedLabelRecognizerSettings labelSettings;
```

### documentSettings

Specifies the settings for the `DynamsoftDocumentNormalizer` task with a [`SimplifiedDocumentNormalizerSettings`]({{ site.ddn_android_api }}simplified-document-normalizer-settings.html) object.

```java
SimplifiedDocumentNormalizerSettings documentSettings;
```
