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

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`capturedResultItemTypes`](#capturedresultitemtypes) | *int* | Specifies the type(s) of CapturedItem(s) that will be captured. |
| [`roi`](#roi) | *[Quadrilateral](../../core/basic-structures/quadrilateral.md)* | Specifies the region of interest (ROI) where the image capture and recognition will take place. |
| [`roiMeasuredInPercentage`](#roimeasuredinpercentage) | *boolean* | Specifies whether the ROI is measured in pixels or as a percentage of the image size. |
| [`maxParallelTasks`](#maxparalleltasks) | *int* | Specifies the maximum number of parallel tasks that can be used for image capture and recognition. |
| [`minImageCaptureInterval`](#minimagecaptureinterval) | *int* | Set the minimum capture interval. It is measured in millisecond. |
| [`timeout`](#timeout) | *int* | Specifies the maximum time (in milliseconds) allowed for image capture and recognition. |
| [`barcodeSettings`](#barcodesettings) | *SimplifiedBarcodeReaderSettings \** | Specifies the settings for barcode recognition. |
| [`labelSettings`](#labelsettings) | *SimplifiedLabelRecognizerSettings \** | Specifies the settings for label recognition. |

### capturedResultItemTypes

Specifies the type(s) of CapturedItem(s) that will be captured.

```java
int capturedResultItemTypes;
```

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

Specifies the settings for barcode recognition.

```java
SimplifiedBarcodeReaderSettings barcodeSettings;
```

### labelSettings

Specifies the settings for label recognition.

```java
SimplifiedLabelRecognizerSettings labelSettings;
```
