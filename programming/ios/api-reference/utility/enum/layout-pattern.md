---
layout: default-layout
title: LayoutPattern - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration LayoutPattern of Dynamsoft Capture Vision iOS edition describes the layout pattern for quadrilateral analysis.
keywords: layout pattern
codeAutoHeight: true
---

# Enumeration LayoutPattern

`LayoutPattern` describes the layout pattern for quadrilateral analysis.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
typedef NS_ENUM(NSInteger, DSLayoutPattern) {
   /**Algorithm automatically detects the best layout pattern.*/
   DSLayoutPatternUnknown = 0,
   /**Elements are organized into sequential lines (rows or columns).*/
   DSLayoutPatternLines = 1,
   /**Elements are organized into a strict grid/matrix structure.*/
   DSLayoutPatternMatrix = 2
} NS_SWIFT_NAME(LayoutPattern);
```
2. 
```swift
enum LayoutPattern : Int {
   /**Algorithm automatically detects the best layout pattern.*/
   case unknown = 0
   /**Elements are organized into sequential lines (rows or columns).*/
   case lines = 1
   /**Elements are organized into a strict grid/matrix structure.*/
   case matrix = 2
}
```
