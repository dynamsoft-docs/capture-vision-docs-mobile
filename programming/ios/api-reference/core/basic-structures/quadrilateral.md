---
layout: default-layout
Title: DSQuadrilateral - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSQuadrilateral of Dynamsoft Core Module represents a quadrilateral shape in 2D space, which contains an array of four CGPoint, representing the vertices of the quadrilateral.
Keywords: quadrilateral, shape, 2D space, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSQuadrilateral

The `DSQuadrilateral` class represents a quadrilateral shape in 2D space, which contains an array of four CGPoint, representing the vertices of the quadrilateral.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSQuadrilateral : NSObject
```
2. 
```swift
class Quadrilateral : NSObject
```

## Attribute Summaries

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *NSArray* |Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex. |

## Method Summaries

| Method | Description |
| ------ | ----------- |
| [`contains`](#contains) | Check whether the input point is contained by the quadrilateral. |
| [`getBoundingRect`](#getboundingrect) | Get the bounding rectangle of the quadrilateral. |
| [`getCentrePoint`](#getcentrepoint) | Get the centre point of the quadrilateral. |
| [`getArea`](#getarea) | Get the area of the quadrilateral. |

## Attribute Details

### points

Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, copy) NSArray *points;
```
2. 
```swift
var points: [CGPoint] { get set }
```

## Method Details

## contains

Check whether the input point is contained by the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)contains:(CGPoint)point;
```
2. 
```swift
func contains(_ point: CGPoint) -> Bool
```

**Parameters**

`point`: Input a point.

**Return Value**

A `BOOL` value that indicates whether the point is contained by the quadrilateral.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
BOOL result = [quadrilateral contains:point];
```
2. 
```swift
let result = quadrilateral.contains(point)
```

## getBoundingRect

Get the bounding rectangle of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (CGRect)getBoundingRect;
```
2. 
```swift
func getBoundingRect() -> CGRect
```

**Return Value**

The bounding rectangle of the quadrilateral.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
CGRect rect = [quadrilateral getBoundingRect];
```
2. 
```swift
let rect = quadrilateral.getBoundingRect()
```

## getCentrePoint

Get the centre point of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (CGPoint)getCentrePoint;
```
2. 
```swift
func getCentrePoint() -> CGPoint
```

**Return Value**

The centre point of the quadrilateral.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
CGPoint center = [quadrilateral getCentrePoint];
```
2. 
```swift
let center = quadrilateral.getCentrePoint()
```

## getArea

Get the area of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getArea;
```
2. 
```swift
func getArea() -> Int
```

**Return Value**

The area of the quadrilateral.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSInteger area = [quadrilateral getArea];
```
2. 
```swift
let area = quadrilateral.getArea()
```