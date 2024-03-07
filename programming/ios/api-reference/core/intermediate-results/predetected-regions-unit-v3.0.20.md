---
layout: default-layout
title: DSPredetectedRegionsUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSPredetectedRegionsUnit of Dynamsoft Core Module represents a unit that contains a collection of pre-detected regions.
keywords: pre-detected regions, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSPredetectedRegionsUnit

The `DSPredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSPredetectedRegionsUnit: DSIntermediateResultUnit
```
2. 
```swift
class PredetectedRegionsUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`predetectedRegions`](#predetectedregions) | *NSArray<DSPredetectedRegionElement*> \** | An array of `DSPredetectedRegionElement` objects. |

### predetectedRegions

An array of `DSPredetectedRegionElement` objects.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSArray<DSPredetectedRegionElement*>* predetectedRegions;
```
2. 
```swift
var predetectedRegions: [PredetectedRegionElement]? { get set }
```
