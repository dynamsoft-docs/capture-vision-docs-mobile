---
layout: default-layout
title: FilterType - Dynamsoft Utility iOS Enumerations
description: The enumeration FilterType of Dynamsoft Utility iOS edition describes the specified image filter applied to an input image.
keywords: image filter
codeAutoHeight: true
---

# Enumeration FilterType

`FilterType` describes the specified image filter applied to an input image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
typedef NS_ENUM(NSInteger, DSFilterType) {
   /**High-pass filter: Enhances edges and fine details by attenuating low-frequency components.*/
   DSFilterTypeHighPass,
   /**Sharpen filter: Increases contrast along edges to make the image appear more defined.*/
   DSFilterTypeSharpen,
   /**Smooth (blur) filter: Reduces noise and detail by averaging pixel values, creating a softening effect.*/
   DSFilterTypeSmooth
} NS_SWIFT_NAME(FilterType);
```
2. 
```swift
enum FilterType : Int {
   /**High-pass filter: Enhances edges and fine details by attenuating low-frequency components.*/
   case highPass
   /**Sharpen filter: Increases contrast along edges to make the image appear more defined.*/
   case sharpen
   /**Smooth (blur) filter: Reduces noise and detail by averaging pixel values, creating a softening effect.*/
   case smooth
}
```
