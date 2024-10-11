---
layout: default-layout
title: DSContour - Dynamsoft Core Module iOS Edition API Reference
description: The class DSContour of Dynamsoft Core Module represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.
keywords: contour, 2D space, CPoint, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSContour

The `Contour` class represents a contour made up of multiple points.

## Definition

*Assembly:* DynamsoftCore.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSContour : NSObject
```
2. 
```swift
class Contour : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *NSArray \** | An array of `Point` objects defining the vertices of the contour. |

### points

An array of `Point` objects defining the vertices of the contour.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy) NSArray *points;
```
2. 
```swift
var points: [Point] { get set }
```
