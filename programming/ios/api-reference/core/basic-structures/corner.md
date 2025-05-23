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

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`type`](#type) | *DSCornerType* | The type of the corner, represented by the enumeration [`DSCornerType`]({{ site.dcv_ios_api }}core/enum/corner-type.html?lang=objc,swift). |
| [`intersection`](#intersection) | *CGPoint* | The point of intersection of the two lines forming the corner. |
| [`line1`](#line1) | *DSLineSegment \** | The first line segment forming the corner. |
| [`line2`](#line2) | *DSLineSegment \** | The second line segment forming the corner. |

### type

The type of the corner, represented by the enumeration [`DSCornerType`]({{ site.dcv_ios_api }}core/enum/corner-type.html?lang=objc,swift).

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

The first line segment forming the corner.

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

The second line segment forming the corner.

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
