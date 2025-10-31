---
layout: default-layout
title: DSEdge - Dynamsoft Core Module iOS Edition API Reference
description: The class DSEdge of Dynamsoft Core Module represents an edge of candidate quadrilaterals, which consists of two corners.
keywords: edge, quadrilateral, corner, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSEdge

The `DSEdge` class represents an edge defined by two `Corners`.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSEdge : NSObject
```
2. 
```swift
class Edge : NSObject
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startCorner`](#startcorner) | *DSCorner \** | The starting corner of the edge. |
| [`endCorner`](#endcorner) | *DSCorner \** | The ending corner of the edge. |

| Method | Description |
| ------ | ----------- |
| [`initWithStartCorner`](#initwithstartcorner) | The constructor. Creates an instance from start corner and end corner. |

### startCorner

The starting corner of the edge.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) DSCorner *startCorner;
```
2. 
```swift
var startCorner: Corner? { get set }
```

### endCorner

The ending corner of the edge.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) DSCorner *endCorner;
```
2. 
```swift
var endCorner: Corner? { get set }
```

### initWithStartCorner

The constructor. Creates an instance from start corner and end corner.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithStartCorner:(DSCorner *)startCorner
                          endCorner:(DSCorner *)endCorner;
```
2. 
```swift
init(startCorner: Corner, endCorner: Corner)
```
