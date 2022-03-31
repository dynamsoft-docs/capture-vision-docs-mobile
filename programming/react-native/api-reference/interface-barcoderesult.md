---
layout: default-layout
title: Interface TextResult of React-Native Dynamsoft Capture Vision
description: The interface of TextResult result
keywords: Interface TextResult, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: TextResult
---

# BarcodeResult

Interface `BarcodeResult`. The return value when barcode is detected. It stores the barcode information including barcode text and barcode formats.

```js
export interface TextResult {
    /**
     * The barcode text.
     */
    barcodeText: string;
    /**
     * Barcode type in string.
     */
    barcodeFormatString: string;
    /**
     * The corresponding localization result.
     */
    localizationResult: LocalizationResult;
}
```
