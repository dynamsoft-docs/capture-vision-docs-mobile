---
layout: default-layout
title: Interface Region of Dynamsoft Capture Vision Flutter Edition
description: The interface of region
keywords: Interface Region, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Region
---

# Region

Interface `Region`.

```dart
class Region extends Serializer {
    /// The y coordinate of the Top border of the region.
    int regionTop;
    /// The y coordinate of the Bottom border of the region.
    int regionBottom;
    /// The x coordinate of the left border of the region.
    int regionLeft;
    /// The x coordinate of the right border of the region.
    int regionRight;
    /// If measured by percentage, the above values will be recognized as percentage (1 to 100).
    /// Otherwise, the above values will be recognized as pixel length.
    bool regionMeasuredByPercentage;
}
```

## Related API(s)

- [`DCVCameraEnhancer.setScanRegion`](camera-enhancer.md#setscanregion)
