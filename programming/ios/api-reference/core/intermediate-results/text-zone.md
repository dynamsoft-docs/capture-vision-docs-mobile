---
layout: default-layout
title: DSTextZone - Dynamsoft Core Module iOS Edition API Reference
description: The class DSTextZone of Dynamsoft Core Module represents a single text zone.
keywords: text zones unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextZone

The `TextZone` class describes a text zone.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSTextZone: NSObject
```
2. 
```swift
class TextZone: NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`location`](#location) | *DSQuadrilateral * \** | The location of the text zone. |
| [`charContoursIndices`](#charcontourindices) | *NSArray * \** | The indices of the character contours. |

### location

The location of the text zone.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, copy) DSQuadrilateral * location;
```
2. 
```swift
var location: Quadrilateral? { get set }
```

### charContourIndices

The indices of the character contours.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSArray * charContoursIndices;
```
2. 
```swift
var charContoursIndices: [Int]? { get set }
```
