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

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`location`](#location) | *DSQuadrilateral \** | The location info of the element that defined in DSQuadrilateral. |
| [`referencedElement`](#referencedelement) | *DSRegionObjectElement \** | The referenced element that supports the capturing of this element. |
| [`regionObjectElementType`](#regionobjectelementtype) | *DSRegionObjectElementType* | The type of the element. |

### location

The location info of the element that defined in DSQuadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy) DSQuadrilateral *location;
```
2. 
```swift
var location: DSQuadrilateral? { get set }
```

### referencedElement

The referenced element that supports the capturing of this element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable, readonly) DSRegionObjectElement *referencedElement;
```
2. 
```swift
var referencedElement: RegionObjectElement? { get }
```

### regionObjectElementType

The type of the element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) DSRegionObjectElementType regionObjectElementType;
```
2. 
```swift
var regionObjectElementType: EnumRegionObjectElementType { get }
```
