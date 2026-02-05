---
layout: default-layout
title: IdentityProcessor - Dynamsoft Identity Utility Android Edition API Reference
description: The class IdentityProcessor of Dynamsoft Identity Utility Android is a utility class for processing identity documents. It provides functionality for finding precise portrait zones.
keywords: identity processor, portrait zone, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IdentityProcessor

The `IdentityProcessor` class is a utility class for processing identity documents. It provides functionality for analyzing and extracting information from identity documents.

## Definition

*Namespace:* com.dynamsoft.diu

*Assembly:* DynamsoftIdentityUtility.aar

```java
class IdentityProcessor
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`findPrecisePortraitZone`](#findpreciseportraitzone) | Finds the precise portrait zone from intermediate result units. |

### findPrecisePortraitZone

Finds the precise portrait zone from intermediate result units.

```java
Quadrilateral findPrecisePortraitZone(ScaledColourImageUnit scaledColourImgUnit, LocalizedTextLinesUnit localizedTextLinesUnit, RecognizedTextLinesUnit recognizedTextLinesUnit, DetectedQuadsUnit detectedQuadsUnit, DeskewedImageUnit deskewedImageUnit) throws UtilityException;
```

**Parameters**

`[in] scaledColourImgUnit`: The [`ScaledColourImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/scaled-down-colour-image-unit.html) containing the scaled color image.

`[in] localizedTextLinesUnit`: The [`LocalizedTextLinesUnit`]({{ site.dlr_android_api }}localized-text-lines-unit.html) containing localized text line information.

`[in] recognizedTextLinesUnit`: The [`RecognizedTextLinesUnit`]({{ site.dlr_android_api }}recognized-text-lines-unit.html) containing recognized text line information.

`[in] detectedQuadsUnit`: The [`DetectedQuadsUnit`]({{ site.ddn_android_api }}detected-quads-unit.html) containing detected quadrilateral information.

`[in] deskewedImageUnit`: The [`DeskewedImageUnit`]({{ site.ddn_android_api }}transformed-grayscale-image-unit.html) containing the deskewed image.

**Return Value**

A [`Quadrilateral`]({{ site.dcv_android_api }}core/basic-structures/quadrilateral.html) object representing the precise portrait zone boundaries.

**Exception**

A [`UtilityException`]({{ site.dcv_android_api }}utility/utility-exception.html) will be thrown if an error occurs during processing.
