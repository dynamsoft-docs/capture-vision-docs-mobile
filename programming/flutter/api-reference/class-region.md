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
    final int regionTop;
    /// The y coordinate of the Bottom border of the region.
    final int regionBottom;
    /// The x coordinate of the left border of the region.
    final int regionLeft;
    /// The x coordinate of the right border of the region.
    final int regionRight;
    /// If measured by percentage, the above values will be recognized as percentage (1 to 100).
    /// Otherwise, the above values will be recognized as pixel length.
    final bool regionMeasuredByPercentage;
}
```

## Related API(s)

- [`DynamsoftCameraView.scanRegion`](camera-view.md#scanregion)
