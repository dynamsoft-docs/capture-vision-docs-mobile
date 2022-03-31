---
layout: default-layout
title: Interface BarcodeLocationResult of React-Native Dynamsoft Capture Vision
description: The interface of barcode location result
keywords: Interface BarcodeLocationResult, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: BarcodeLocationResult
---

# BarcodeLocationResult

Interface `BarcodeLocationResult`. The location of a quadrilateral area. It can be the location of a decoded barcode, a recognized label or a deteced document area

```js
export interface BarcodeLocationResult {
    /**
     * The angle of a barcode. Values range from 0 to 360.
     */
    angle: number;
    /**
     * The coordinates of the quadrilateral points.
     */
    location: Quadrilateral;
}
//# sourceMappingURL=BarcodeLocationResult.d.ts.map
```
