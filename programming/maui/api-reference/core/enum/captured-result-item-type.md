---
layout: default-layout
title: EnumCapturedResultItemType - Dynamsoft Vision Router MAUI Enumerations
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
    OriginalImage = 1 << 0,
    /** The type of the CapturedResultItem is "barcode". */
    Barcode = 1 << 1,
    /** The type of the CapturedResultItem is "text line". */
    TextLine = 1 << 2,
    /** The type of the CapturedResultItem is "detected quad". */
    DetectedQuad = 1 << 3,
    /** The type of the CapturedResultItem is "normalized image". */
    DeskewedImage = 1 << 4,
    /** The type of the CapturedResultItem is "parsed result". */
    ParsedResult = 1 << 5,
    /** The type of the CapturedResultItem is "Enhanced image". */
    EnhancedImage = 1 << 6
}
```
