---
layout: default-layout
title: RegionObjectElementType - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration RegionObjectElementType of Dynamsoft Capture Vision iOS describes the types of RegionObjectElement.
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
   DSRegionObjectElementTypePredetectedRegion,
   /**The type of subclass LocalizedBarcodeElement.*/
   DSRegionObjectElementTypeLocalizedBarcode,
   /**The type of subclass DecodedBarcodeElement.*/
   DSRegionObjectElementTypeDecodedBarcode,
   /**The type of subclass LocalizedTextLineElement.*/
   DSRegionObjectElementTypeLocalizedTextLine,
   /**The type of subclass RecognizedTextLineElement.*/
   DSRegionObjectElementTypeRecognizedTextLine,
   /**The type of subclass DetectedQuadElement.*/
   DSRegionObjectElementTypeDetectedQuad,
   /**The type of subclass DeskewedImageElement.*/
   DSRegionObjectElementTypeDeskewedImage,
   /**The type of subclass EnhancedImageElement.*/
   DSRegionObjectElementTypeEnhancedImage
};
```
>
```swift
public enum RegionObjectElementType : Int
{
   /**The type of subclass PredetectedRegionElement.*/
   case predetectedRegion
   /**The type of subclass LocalizedBarcodeElement.*/
   case localizedBarcode
   /**The type of subclass DecodedBarcodeElement.*/
   case decodedBarcode
   /**The type of subclass LocalizedTextLineElement.*/
   case localizedTextLine
   /**The type of subclass RecognizedTextLineElement.*/
   case recognizedTextLine
   /**The type of subclass DetectedQuadElement.*/
   case detectedQuad
   /**The type of subclass DeskewedImageElement.*/
   case deskewedImag
   /**The type of subclass EnhancedImageElement.*/
   case enhancedImage
}
```
