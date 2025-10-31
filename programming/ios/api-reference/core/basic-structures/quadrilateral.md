---
layout: default-layout
title: DSQuadrilateral - Dynamsoft Core Module iOS Edition API Reference
description: The class DSQuadrilateral of Dynamsoft Core Module represents a quadrilateral shape in 2D space, which contains an array of four CGPoint, representing the vertices of the quadrilateral.
keywords: quadrilateral, shape, 2D space, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSQuadrilateral

The `DSQuadrilateral` class represents a quadrilateral defined by four points.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *NSArray* | An array of four `Point` objects defining the vertices of the quadrilateral. |
| [`id`](#id) | *NSInteger* | The ID of the quadrilateral. |
| [`boundingRect`](#boundingrect) | *CGRect* | Get the bounding rectangle of the quadrilateral. |
| [`centrePoint`](#centrepoint) | *CGPoint* | Get the centre point of the quadrilateral. |
| [`area`](#area) | *NSUInteger* | Get the area of the quadrilateral. |

| Method | Description |
| ------ | ----------- |
| [`initWithPointArray(points:)`](#initwithpointarraypoints) | The constructor. Creates a quadrilateral from an array of points. |
| [`initWithPointArray(points:quadId:)`](#initwithpointarraypointsquadid) | The constructor. Creates a quadrilateral from an array of points and an ID. |
| [`contains`](#contains) | Check whether the input point is contained by the quadrilateral. |

### points

An array of four `Point` objects defining the vertices of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, copy) NSArray<NSValue *> *points;
```
2. 
```swift
var points: [NSValue] { get }
```

### id

The ID of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger quadId;
```
2. 
```swift
var quadId: Int { get set }
```

### boundingRect

Get the bounding rectangle of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) CGRect boundingRect;
```
2. 
```swift
var boundingRect: CGRect { get }
```

**Return Value**

The bounding rectangle of the quadrilateral.

### centrePoint

Get the centre point of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) CGPoint centrePoint;
```
2. 
```swift
var centrePoint: CGPoint { get }
```

**Return Value**

The centre point of the quadrilateral.

### area

Get the area of the quadrilateral.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) NSUInteger area;
```
2. 
```swift
var area: Int { get }
```

**Return Value**

The area of the quadrilateral.

### initWithPointArray(points:)

The constructor. Creates a quadrilateral from an array of points.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithPointArray:(NSArray<NSValue *> *)points;
```
2. 
```swift
init(points: [NSValue])
```

### initWithPointArray(points:quadId:)

The constructor. Creates a quadrilateral from an array of points and an ID.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithPointArray:(NSArray<NSValue *> *)points quadId:(NSInteger)quadId;
```
2. 
```swift
init(points: [NSValue], quadId: Int)
```

### contains

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
