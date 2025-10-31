---
layout: default-layout
title: DSRegionObjectElement - Dynamsoft Core Module iOS Edition API Reference
description: The class DSRegionObjectElement of Dynamsoft Core Module represents an element of a region object in 2D space, which provides the interface for region object elements.
keywords: region object element, 2D space, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRegionObjectElement

The `DSRegionObjectElement` class represents a basic element of a region object, including its type, location and reference to another element.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSRegionObjectElement : NSObject
```
2. 
```swift
class RegionObjectElement : NSObject
```

## Methods

| Method | Description |
|------- |-------------|
| [`getLocation`](#getlocation) | Gets the location of the region object, represented as a quadrilateral. |
| [`getReferencedElement`](#getreferencedelement) | Gets the referenced element that supports the capturing of this element. |
| [`getRegionObjectElementType`](#gettype) | Gets the type of the region object element, defined by the enumeration [`DSRegionObjectElementType`]({{ site.dcv_ios_api }}core/enum/region-object-element-type.html?lang=objc,swift). |
| [`getImageData`](#getimagedata) | Gets the original image that produce this element. |

### getLocation

Gets the location of the region object, represented as a [`Quadrilateral`]({{ site.dcv_ios_api }}core/basic-structures/quadrilateral.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(DSQuadrilateral*)getLocation;
```
2. 
```swift
func getLocation() -> DSQuadrilateral?
```

**Return Value**

The location info of the element that defined in DSQuadrilateral.

### getReferencedElement

Get the referenced element that supports the capturing of this element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSRegionObjectElement*)getReferencedElement;
```
2. 
```swift
func getReferencedElement() -> RegionObjectElement?
```

**Return Value**

The referenced element that supports the capturing of this element.

### getType

Gets the type of the region object element, defined by the enumeration [`DSRegionObjectElementType`]({{ site.dcv_ios_api }}core/enum/region-object-element-type.html?lang=objc,swift).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSRegionObjectElementType)getType;
```
2. 
```swift
func getType() -> RegionObjectElementType
```

**Return Value**

The type of the region object element.

### getImageData

Gets the original image that produce this element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSImageData *)getImageData;
```
2. 
```swift
func getImageData() -> ImageData?
```

**Return Value**

A `DSImageData` object represents the original image that produce this element.
