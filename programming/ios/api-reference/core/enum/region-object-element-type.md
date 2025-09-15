---
layout: default-layout
title: RegionObjectElementType - Dynamsoft Core Enumerations
description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
keywords: Region object element type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RegionObjectElementType
codeAutoHeight: true
---

# Enumeration RegionObjectElementType

`RegionObjectElementType` specifies the exact subclass type within the `RegionObjectElement` hierarchy. This enumeration facilitates the identification and differentiation of various processed elements in an image.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSRegionObjectElementType)
{
   /**The type of subclass PredetectedRegionElement.*/
   DSRegionObjectElementTypePredetectedRegion = 0,
   /**The type of subclass LocalizedBarcodeElement.*/
   DSRegionObjectElementTypeLocalizedBarcode = 1,
   /**The type of subclass DecodedBarcodeElement.*/
   DSRegionObjectElementTypeDecodedBarcode = 2,
   /**The type of subclass LocalizedTextLineElement.*/
   DSRegionObjectElementTypeLocalizedTextLine = 3,
   /**The type of subclass RecognizedTextLineElement.*/
   DSRegionObjectElementTypeRecognizedTextLine = 4,
   /**The type of subclass DetectedQuadElement.*/
   DSRegionObjectElementTypeDetectedQuad = 5,
   /**The type of subclass NormalizedImageElement.*/
   DSRegionObjectElementTypeNormalizedImage = 6
};
```
>
```swift
public enum RegionObjectElementType : Int
{
   /**The type of subclass PredetectedRegionElement.*/
   predetectedRegion = 0,
   /**The type of subclass LocalizedBarcodeElement.*/
   localizedBarcode = 1,
   /**The type of subclass DecodedBarcodeElement.*/
   decodedBarcode = 2,
   /**The type of subclass LocalizedTextLineElement.*/
   localizedTextLine = 3,
   /**The type of subclass RecognizedTextLineElement.*/
   recognizedTextLine = 4,
   /**The type of subclass DetectedQuadElement.*/
   detectedQuad = 5,
   /**The type of subclass NormalizedImageElement.*/
   normalizedImage = 6
}
```
