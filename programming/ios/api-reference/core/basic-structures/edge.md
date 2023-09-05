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

The `DSEdge` class represents an edge of candidate quadrilaterals, which consists of two corners.

## Definition

*Assembly:* DynamsoftCore.framework

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

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startCorner`](#startcorner) | *DSCorner \** | The start corner of the edge. |
| [`endCorner`](#endcorner) | *DSCorner \** | The end corner of the edge. |

### startCorner

The start corner of the edge.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable) DSCorner *startCorner;
```
2. 
```swift
var startCorner: Corner? { get set }
```

### endCorner

The end corner of the edge.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable) DSCorner *endCorner;
```
2. 
```swift
var endCorner: Corner? { get set }
```
