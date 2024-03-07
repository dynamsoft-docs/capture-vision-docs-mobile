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

The `DSRegionObjectElement` class represents an element of a region object in 2D space, which provides the interface for region object elements.

## Definition

*Assembly:* DynamsoftCore.framework

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
| [`getLocation`](#getlocation) | Returns the location info of the element. |
| [`setLocation`](#setlocation) | Sets the location info of the element. |
| [`getReferencedElement`](#getreferencedelement) | Returns the referenced element that supports the capturing of this element. |
| [`getRegionObjectElementType`](#getregionobjectelementtype) | Returns the type of the element. |

### getLocation

Get the location info of the element.

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

### setLocation

Set the location info of the element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)setLocation:(DSQuadrilateral *)location;
```
2. 
```swift
func setLocation(_ location: DSQuadrilateral?)
```

**Parameters**

`location`: The location info of the element that defined in DSQuadrilateral.

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

### getRegionObjectElementType

Get the type of the element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(DSRegionObjectElementType)getRegionObjectElementType;
```
2. 
```swift
func getRegionObjectElementType() -> RegionObjectElementType
```

**Return Value**

The type of the element.
