---
layout: default-layout
title: Use multi-frame cross filter - Dynamsoft Capture Vision Android Edition
description: This page introduce how to use the multi-frame cross filter feature of Dynamsoft Capture Vision Android Edition.
keywords: Android, multi-frame, filter
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# How to Use Multi-Frame Cross Filter

[`MultiFrameCrossFilter`]({{ site.dcv_android_api }}utility/multi-frame-cross-filter.html) is a class under `DynamsoftUtility` library. It provides APIs for users to implement filter features based on the neighbouring video frames.

| Filter Type | Description |
| ----------- | ----------- |
| Deduplication | Filter out the duplicate results in the period of `DuplicateForgetTime`. |
| Cross Verification | Verify the accuracy of the results based on the neighbouring video frames. |

## Add a Filter for a Single Result type

You can trigger the `enable` methods to enable/disable the filter features. You have to include a `resultType` parameter when triggering a `enable` method. It is used to specify which kind of result you want to implement the filter feature. For example, if you want to implement both the **Deduplication** and **Cross Verification** filter for the text line recognition results, you can use the following code:

```java
MultiFrameResultCrossFilter filter = new MultiFrameResultCrossFilter();
filter.enableResultCrossVerification(EnumCapturedResultItemType.CRIT_TEXT_LINE, true);
filter.enableResultDeduplication(EnumCapturedResultItemType.CRIT_TEXT_LINE, true);
// captureVisionRouter is a CaptureVisionRouter object.
// Remember to add the filter to the CaptureVisionRouter. Otherwise, it is not effective.
captureVisionRouter.addResultFilter(filter);
```

## Add a Filter for Multiple Result types

If you are going to implement the **Cross Verification** filter on the text line recognition results and **Deduplication** filter on both the text line recognition results and the barcode reading results, you can use the following code:

```java
MultiFrameResultCrossFilter filter = new MultiFrameResultCrossFilter();
filter.enableResultCrossVerification(EnumCapturedResultItemType.CRIT_TEXT_LINE, true);
filter.enableResultDeduplication(EnumCapturedResultItemType.CRIT_TEXT_LINE | EnumCapturedResultItemType.CRIT_BARCODE, true);
// captureVisionRouter is a CaptureVisionRouter object.
// Remember to add the filter to the CaptureVisionRouter. Otherwise, it is not effective.
captureVisionRouter.addResultFilter(filter);
```

## Disable the Filter

To disable the filter feature, for example disable the **Deduplication** filter on the text line recognition results, you can add the following code:

```java
filter.enableResultDeduplication(EnumCapturedResultItemType.CRIT_TEXT_LINE | EnumCapturedResultItemType.CRIT_BARCODE, false);
```

To remove all the filter features, you can use the remove method:

```java
// captureVisionRouter is a CaptureVisionRouter object.
captureVisionRouter.removeResultFilter(filter);
```
