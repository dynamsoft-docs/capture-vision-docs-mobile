---
layout: default-layout
title: Buffered Items APIs of CaptureVisionRouter - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: Buffered items APIs references for DCV Android Edition.
keywords: capture vision, intermediate result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Buffered Items

## Method Summary

| Method | Description |
|------- |-------------|
| [`getBufferedItemsManager`](#getbuffereditemsmanager) | Returns the manager instance of buffered items. |

## Method Details

### getBufferedItemsManager

Returns the manager instance of buffered items.

```java
BufferedItemsManager getBufferedItemsManager();
```

**Return Value**

Returns the manager instance of buffered items.

**Remarks**

When the maximum number of buffered items is set to greater than 0, item buffering is enabled. Currently only character items can be buffered.
