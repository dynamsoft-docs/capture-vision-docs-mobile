---
layout: default-layout
title: MeasureUnit - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration MeasureUnit of Dynamsoft Capture Vision iOS edition describes the unit of measurement for a value.
keywords: measure unit, pixel, percentage
codeAutoHeight: true
---

# Enumeration MeasureUnit

`MeasureUnit` describes the unit of measurement for a value.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
typedef NS_ENUM(NSInteger, DSMeasureUnit) {
   /**The value is an absolute pixel count.*/
   DSMeasureUnitPixel = 0,
   /**The value is a percentage of the reference dimension (e.g. 25 = 25%).*/
   DSMeasureUnitPercentage = 1
} NS_SWIFT_NAME(MeasureUnit);
```
2. 
```swift
enum MeasureUnit : Int {
   /**The value is an absolute pixel count.*/
   case pixel = 0
   /**The value is a percentage of the reference dimension (e.g. 25 = 25%).*/
   case percentage = 1
}
```
