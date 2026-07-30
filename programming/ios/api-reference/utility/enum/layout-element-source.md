---
layout: default-layout
title: LayoutElementSource - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration LayoutElementSource of Dynamsoft Capture Vision iOS edition describes the origin of a layout element.
keywords: layout element source
codeAutoHeight: true
---

# Enumeration LayoutElementSource

`LayoutElementSource` describes the origin of a layout element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
typedef NS_ENUM(NSInteger, DSLayoutElementSource) {
   /**No element exists at this logical grid position.*/
   DSLayoutElementSourceNone = 0,
   /**Element is provided from the original input array.*/
   DSLayoutElementSourceInput = 1,
   /**Element is reconstructed or filled in by the algorithm.*/
   DSLayoutElementSourceInferred = 2
} NS_SWIFT_NAME(LayoutElementSource);
```
2. 
```swift
enum LayoutElementSource : Int {
   /**No element exists at this logical grid position.*/
   case none = 0
   /**Element is provided from the original input array.*/
   case input = 1
   /**Element is reconstructed or filled in by the algorithm.*/
   case inferred = 2
}
```
