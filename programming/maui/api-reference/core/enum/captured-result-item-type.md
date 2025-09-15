---
layout: default-layout
title: EnumCapturedResultItemType - Dynamsoft Vision Router MAUI Edition
description: The enumeration CapturedResultItemType of Dynamsoft Vision Router describes the type of CapturedResultItem.
keywords: capture result item type, multi-frame cross filter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CapturedResultItemType
---

# Enumeration CapturedResultItemType

`CapturedResultItemType` describes the camera position.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public enum EnumCapturedResultItemType
{
    /** The type of the CapturedResultItem is "original image". */
    CRIT_ORIGINAL_IMAGE = 1 << 0,
    /** The type of the CapturedResultItem is "barcode". */
    CRIT_BARCODE = 1 << 1,
    /** The type of the CapturedResultItem is "text line". */
    CRIT_TEXT_LINE = 1 << 2,
    /** The type of the CapturedResultItem is "detected quad". */
    CRIT_DETECTED_QUAD = 1 << 3,
    /** The type of the CapturedResultItem is "normalized image". */
    CRIT_NORMALIZED_IMAGE = 1 << 4,
    /** The type of the CapturedResultItem is "parsed result". */
    CRIT_PARSED_RESULT = 1 << 5
}
```
