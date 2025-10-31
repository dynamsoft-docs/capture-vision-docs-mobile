---
layout: default-layout
title: DSLineSegment - Dynamsoft Core Module iOS Edition API Reference
description: The class DSLineSegment of Dynamsoft Core Module represents a line segment in 2D space, which contains the start point and end point of the line segment.
keywords: line segment, 2D, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLineSegment

The `DSLineSegment` class represents a line segment defined by two `Points`.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLineSegment : NSObject
```
2. 
```swift
class LineSegment : NSObject
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startPoint`](#startpoint) | *CGPoint* | The starting point of the line segment. |
| [`endPoint`](#endpoint) | *CGPoint* | The ending point of the line segment. |
| [`id`](#id) | *int* | The ID of the line segment. |

| Methods | Description |
| ------- | ----------- |
| [`initWithStartPoint`](#initwithstartpoint) | The constructor. Creates an instance from start point, end point and line ID. |

### startPoint

The starting point of the line segment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGPoint startPoint;
```
2. 
```swift
var startPoint: CGPoint { get set }
```

### endPoint

The ending point of the line segment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGPoint endPoint;
```
2. 
```swift
var endPoint: CGPoint { get set }
```

### id

The ID of the line segment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger lineId;
```
2. 
```swift
var lineId: Int { get set }
```

### initWithStartPoint

The constructor. Creates an instance from start point, end point and line ID.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithStartPoint:(CGPoint)startPoint
                          endPoint:(CGPoint)endPoint
                            lineId:(NSInteger)lineId;
```
2. 
```swift
init(startPoint: CGPoint, endPoint: CGPoint, lineId: Int)
```
