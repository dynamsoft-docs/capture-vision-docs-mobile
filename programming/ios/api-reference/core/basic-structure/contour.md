---
layout: default-layout
Title: DSContour - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSContour of Dynamsoft Core Module represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.
Keywords: contour, 2D space, CPoint, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSContour

The `DSContour` class represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.

## Definition

*Assembly:* DynamsoftCore.framework

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
| [`points`](#points) | *NSArray \** | An array includes all vertices of the contour. |

### points

An array includes all vertices of the contour.

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
var points: [CPoint] { get set }
```
