---
layout: default-layout
title: DSLineSegmentsUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSLineSegmentsUnit of Dynamsoft Core Module represents a collection of line segments in 2D space.
keywords: line segments, 2D space, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLineSegmentsUnit

The `DSLineSegmentsUnit` class represents a collection of line segments in 2D space. It is a derived class of `DSIntermediateResultUnit`.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLineSegmentsUnit: DSIntermediateResultUnit
```
2. 
```swift
class LineSegmentsUnit : IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`lineSegments`](#linesegments) | *NSArray<DSLineSegment*>* \** | An array of `DSLineSegment`. |

### lineSegments

An array of `DSLineSegment`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, nullable) NSArray<DSLineSegment*>* lineSegments;
```
2. 
```swift
var lineSegments: [DSLineSegment]? { get set }
```
