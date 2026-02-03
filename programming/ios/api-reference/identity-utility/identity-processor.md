---
layout: default-layout
title: DSIdentityProcessor - Dynamsoft Identity Utility iOS Edition API Reference
description: The class DSIdentityProcessor of Dynamsoft Identity Utility iOS is a utility class for processing identity documents. It provides functionality for finding precise portrait zones.
keywords: identity processor, portrait zone, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIdentityProcessor

The `DSIdentityProcessor` class is a utility class for processing identity documents. It provides functionality for analyzing and extracting information from identity documents.

## Definition

*Assembly:* DynamsoftIdentityUtility.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSIdentityProcessor : NSObject
```
2. 
```swift
class IdentityProcessor : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`findPrecisePortraitZone`](#findpreciseportraitzone) | Finds the precise portrait zone from intermediate result units. |

### findPrecisePortraitZone

Finds the precise portrait zone from intermediate result units.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSQuadrilateral *)findPrecisePortraitZone:(DSScaledColourImageUnit *)scaledColourImgUnit
                             localizedTextLinesUnit:(DSLocalizedTextLinesUnit *)localizedTextLinesUnit
                            recognizedTextLinesUnit:(DSRecognizedTextLinesUnit *)recognizedTextLinesUnit
                                  detectedQuadsUnit:(DSDetectedQuadsUnit *)detectedQuadsUnit
                                  deskewedImageUnit:(DSDeskewedImageUnit *)deskewedImageUnit;
```
2. 
```swift
func findPrecisePortraitZone(scaledColourImgUnit: ScaledColourImageUnit, localizedTextLinesUnit: LocalizedTextLinesUnit, recognizedTextLinesUnit: RecognizedTextLinesUnit, detectedQuadsUnit: DetectedQuadsUnit, deskewedImageUnit: DeskewedImageUnit) -> Quadrilateral?
```

**Parameters**

`scaledColourImgUnit`: The [`DSScaledColourImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/scaled-down-colour-image-unit.html) containing the scaled color image.

`localizedTextLinesUnit`: The [`DSLocalizedTextLinesUnit`]({{ site.dlr_ios_api }}localized-text-lines-unit.html) containing localized text line information.

`recognizedTextLinesUnit`: The [`DSRecognizedTextLinesUnit`]({{ site.dlr_ios_api }}recognized-text-lines-unit.html) containing recognized text line information.

`detectedQuadsUnit`: The [`DSDetectedQuadsUnit`]({{ site.ddn_ios_api }}detected-quads-unit.html) containing detected quadrilateral information.

`deskewedImageUnit`: The [`DSDeskewedImageUnit`]({{ site.ddn_ios_api }}transformed-grayscale-image-unit.html) containing the deskewed image.

**Return Value**

A [`DSQuadrilateral`]({{ site.dcv_ios_api }}core/basic-structures/quadrilateral.html) object representing the precise portrait zone boundaries, or nil if an error occurs.
