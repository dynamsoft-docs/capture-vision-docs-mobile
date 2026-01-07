---
layout: default-layout
title: CapturedResultItemType - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration CapturedResultItemType of Dynamsoft Capture Vision iOS describes all types of captured result item.
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
typedef NS_OPTIONS(NSInteger, DSCapturedResultItemType)
{
   /** Captured result item type original image.*/
   DSCapturedResultItemTypeOriginalImage = 1 << 0,
   /** Captured result item type barcode.*/
   DSCapturedResultItemTypeBarcode = 1 << 1,
   /** Captured result item type text line.*/
   DSCapturedResultItemTypeTextLine = 1 << 2,
   /** Captured result item type detected quad.*/
   DSCapturedResultItemTypeDetectedQuad = 1 << 3,
   /** Captured result item type deskewed image.*/
   DSCapturedResultItemTypeDeskewedImage = 1 << 4,
   /** Captured result item type parsed content.*/
   DSCapturedResultItemTypeParsedResult = 1 << 5,
   /** Captured result item type enhanced image.*/
   DSCapturedResultItemTypeEnhancedImage = 1 << 6
};
```
>
```swift
struct CapturedResultItemType: OptionSet {
   let rawValue: Int
   /** Captured result item type original image.*/
   static let originalImage   = CapturedResultItemType(rawValue: 1 << 0)
   /** Captured result item type barcode.*/
   static let barcode         = CapturedResultItemType(rawValue: 1 << 1)
   /** Captured result item type text line.*/
   static let textLine        = CapturedResultItemType(rawValue: 1 << 2)
   /** Captured result item type detected quad.*/
   static let detectedQuad    = CapturedResultItemType(rawValue: 1 << 3)
   /** Captured result item type deskewed image.*/
   static let deskewedImage   = CapturedResultItemType(rawValue: 1 << 4)
   /** Captured result item type parsed content.*/
   static let parsedResult    = CapturedResultItemType(rawValue: 1 << 5)
   /** Captured result item type enhanced image.*/
   static let enhancedImage   = CapturedResultItemType(rawValue: 1 << 6)
}
```
