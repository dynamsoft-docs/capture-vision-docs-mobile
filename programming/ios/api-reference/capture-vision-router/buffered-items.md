---
layout: default-layout
title: Buffered Items APIs of CaptureVisionRouter - Dynamsoft Capture Vision iOS Edition API Reference
description: Buffered items APIs references for DCV iOS Edition.
keywords: capture vision, intermediate result, Objc, Swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Buffered Items

## Methods

| Method | Description |
|------- |-------------|
| [`getBufferedItemsManager`](#getbuffereditemsmanager) | Gets the buffered items manager to access the buffered character items. |

### getBufferedItemsManager

Gets the `DSBufferedItemsManager` instance to access the buffered character items.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSBufferedItemsManager *)getBufferedItemsManager;
```
2. 
```swift
func getBufferedItemsManager() -> BufferedItemsManager
```

**Return Value**

The `DSBufferedItemsManager` instance.

**Remarks**

When the maximum number of buffered items is set to greater than 0, item buffering is enabled. Currently only character items can be buffered.
