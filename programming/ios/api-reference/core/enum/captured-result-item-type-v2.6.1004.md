---
layout: default-layout
title: CapturedResultItemType - Dynamsoft Core Enumerations
description: The enumeration CapturedResultItemType of Dynamsoft Core describes all types of captured result item.
keywords: Captured result types
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CapturedResultItemType
codeAutoHeight: true
---

# Enumeration CapturedResultItemType

`CapturedResultItemType` defines the various categories of items that can be recognized and captured.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSCapturedResultItemType)
{
   /** The captured result is a original image. You can convert it into a DSOriginalImageResultItem. */
   DSCapturedResultItemTypeOriginalImage = 1,
   /** The captured result is a decoded barcode. You can convert it into a DSBarcodeResultItem. */
   DSCapturedResultItemTypeBarcode = 2,
   /** The captured result is a recognized text line. You can convert it into a DSTextLineResultItem. */
   DSCapturedResultItemTypeTextLine = 4,
   /** The captured result is a detected quadrilateral. You can convert it into a DSDetectedQuadResultItem. */
   DSCapturedResultItemTypeDetectedQuad = 8,
   /** The captured result is a normalized image. You can convert it into a DSNormalizedImageResultItem. */
   DSCapturedResultItemTypeNormalizedImage = 16,
   /** The captured result is a parsed result. You can convert it into a DSParsedResultItem. */
   DSCapturedResultItemTypeParsedResult = 32,
};
```
>
```swift
public enum CapturedResultItemType : Int
{
   /** The captured result is a original image. You can convert it into a DSOriginalImageResultItem. */
   originalImage = 1
   /** The captured result is a decoded barcode. You can convert it into a DSBarcodeResultItem. */
   barcode = 2
   /** The captured result is a recognized text line. You can convert it into a DSTextLineResultItem. */
   textLine = 4
   /** The captured result is a detected quadrilateral. You can convert it into a DSDetectedQuadResultItem. */
   detectedQuad = 8
   /** The captured result is a normalized image. You can convert it into a DSNormalizedImageResultItem. */
   normalizedImage = 16
   /** The captured result is a parsed result. You can convert it into a DSParsedResultItem. */
   parsedResult = 32
};
```
