---
layout: default-layout
title: DSLayoutElement - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSLayoutElement of Dynamsoft Capture Vision iOS edition represents an element in a layout analysis.
keywords: layout element, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLayoutElement

The `DSLayoutElement` class represents an element in a layout analysis.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(LayoutElement)
@interface DSLayoutElement : NSObject
```
2. 
```swift
class LayoutElement : NSObject
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`quad`](#quad) | *DSQuadrilateral \** | Geometric coordinates of the element. |
| [`source`](#source) | *DSLayoutElementSource* | Origin of the element. |

### quad

Geometric coordinates of the element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) DSQuadrilateral *quad;
```
2. 
```swift
var quad: Quadrilateral { get set }
```

### source

Origin of the element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSLayoutElementSource source;
```
2. 
```swift
var source: LayoutElementSource { get set }
```
