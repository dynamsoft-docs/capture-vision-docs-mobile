---
layout: default-layout
title: TargetType - Dynamsoft Core Enumerations
description: The enumeration TargetType of Dynamsoft Core describes target types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TargetType
codeAutoHeight: true
---

# Enumeration TargetType

`TargetType` describes the target types.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSTargetType)
{
   /**The target type of the PDF file is "page". Only available for PDFReadingMode raster.*/
   DSTargetTypePage = 0,
   /**The target type of the PDF file is "image".*/
   DSTargetTypeImage = 1
};
```
>
```swift
public enum TargetType : Int
{
   /**The target type of the PDF file is "page". Only available for PDFReadingMode raster.*/
   page = 0,
   /**The target type of the PDF file is "image".*/
   image = 1
}
```
