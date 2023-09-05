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

The `DSLineSegment` class represents a line segment in 2D space, which contains the start point and end point of the line segment.

## Definition

*Assembly:* DynamsoftCore.framework

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

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startPoint`](#startpoint) | *CGPoint* | The start point of the line segment. |
| [`endPoint`](#endpoint) | *CGPoint* | The end point of the line segment. |

### startPoint

The start point of the line segment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign) CGPoint startPoint;
```
2. 
```swift
var startPoint: CGPoint { get set }
```

### endPoint

The end point of the line segment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign) CGPoint endPoint;
```
2. 
```swift
var endPoint: CGPoint { get set }
```
