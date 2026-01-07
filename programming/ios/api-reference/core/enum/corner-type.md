---
layout: default-layout
title: CornerType - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration CornerType of Dynamsoft Capture Vision iOS describes how the corner is formed by its sides.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CornerType
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSCornerType)
{
   /** The corner is formed by two intersecting line segments. */
   DSCornerTypeNormalIntersected,
   /** The corner is formed by two T intersecting line segments. */
   DSCornerTypeTIntersected,
   /** The corner is formed by two cross intersecting line segments. */
   DSCornerTypeCrossIntersected,
   /** The two line segments are not intersected but they definitely consist a corner. */
   DSCornerTypeNotIntersected
};
```
>
```swift
public enum CornerType : Int
{
   /** The corner is formed by two intersecting line segments. */
   case intersected
   /** The corner is formed by two T intersecting line segments. */
   case tIntersected
   /** The corner is formed by two cross intersecting line segments. */
   case crossIntersected
   /** The two line segments are not intersected but they definitely consist a corner. */
   case notIntersected
};
```
