---
layout: default-layout
title: DSRect - Dynamsoft Core Module iOS Edition API Reference
description: The class DSRect of Dynamsoft Core Module iOS edition represents a rectangle in 2D space, which contains four integer values that specify the top, left, right, and bottom edges of the rectangle.
keywords: rectangle, 2D space, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRect

The `DSRect` class represents a rectangle in 2D space, which contains four integer values that specify the top, left, right, and bottom edges of the rectangle.

## Definition

*Assembly:* DynamsoftCore.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSRect : NSObject
```
2. 
```swift
class Rect : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`top`](#top) | *CGFloat* | The distance between the top of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`left`](#left) | *CGFloat* | The distance between the left of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`right`](#right) | *CGFloat* | The distance between the right of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`bottom`](#bottom) | *CGFloat* | The distance between the bottom of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`measuredInPercentage`](#measuredinpercentage) | *BOOL* | Indicates if the rectangle's measurements are in percentages. |

### top

The distance between the top of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGFloat top
```
2. 
```swift
var top: CGFloat { get set }
```

### left

The distance between the left of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGFloat left
```
2. 
```swift
var left: CGFloat { get set }
```

### right

The distance between the right of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGFloat right
```
2. 
```swift
var right: CGFloat { get set }
```

### bottom

The distance between the bottom of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGFloat bottom
```
2. 
```swift
var bottom: CGFloat { get set }
```

### measuredInPercentage

Sets whether to use percentages to measure the region size.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) BOOL measuredInPercentage
```
2. 
```swift
var measuredInPercentage: Bool { get set }
```
