---
layout: default-layout
title: Interface LocalizationResult of React-Native Dynamsoft Capture Vision
description: The interface of localization result
keywords: Interface LocalizationResult, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: LocalizationResult
---

# LocalizationResult

Interface `LocalizationResult`. The location of a quadrilateral area. It can be the location of a decoded barcode, a recognized label or a deteced document area

```js
export interface LocalizationResult {
    /**
     * The angle of a barcode. Values range from 0 to 360.
     */
    angle: number;
    /**
     * The coordinates of the quadrilateral points.
     */
    location: Quadrilateral;
}
//# sourceMappingURL=localizationresult.d.ts.map
```
