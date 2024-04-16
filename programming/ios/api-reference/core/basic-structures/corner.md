---
layout: default-layout
title: DSCorner - Dynamsoft Core Module iOS Edition API Reference
description: The class DSCorner of Dynamsoft Core Module represents a detected corner, which consists of an intersection and two lines.
keywords: corner, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCorner

The `DSCorner` class represents a corner, typically where two line segments meet.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCorner: NSObject
```
2. 
```swift
class Corner: NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`type`](#type) | *DSCornerType* | The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected. |
| [`intersection`](#intersection) | *CGPoint* | The coordinate of the intersection point of the corner. |
| [`line1`](#line1) | *DSLineSegment \** |One of the lines of the corner. Defined in DSLineSegment. |
| [`line2`](#line2) | *DSLineSegment \** |One of the lines of the corner. Defined in DSLineSegment. |

### type

The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSCornerType type
```
2. 
```swift
var type: DSCornerType { get set }
```

### intersection

The coordinate of the intersection point of the corner.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGPoint intersection
```
2. 
```swift
var intersection: CGPoint { get set }
```

### line1

One of the lines of the corner. Defined in DSLineSegment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSLineSegment *line1;
```
2. 
```swift
var line1: DSLineSegment? { get set }
```

### line2

One of the lines of the corner. Defined in DSLineSegment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSLineSegment *line2;
```
2. 
```swift
var line2: DSLineSegment? { get set }
```
