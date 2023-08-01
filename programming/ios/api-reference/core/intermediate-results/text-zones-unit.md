---
layout: default-layout
Title: DSTextZonesUnit - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSTextZonesUnit of Dynamsoft Core Module represents a unit that contains text zones, which is derived from DSIntermediateResultUnit class.
Keywords: text zones unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextZonesUnit

The `DSTextZonesUnit` class represents a unit that contains text zones, which is derived from `DSIntermediateResultUnit` class.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSTextZonesUnit: DSIntermediateResultUnit
```
2. 
```swift
class TextZonesUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`textZones`](#textzones) | *NSArray<DSQuadrilateral *> \** | An array of DSQuadrilaterals as text zones. |

### textZones

An array of DSQuadrilaterals as text zones.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, nullable) NSArray<DSQuadrilateral *> *textZones;
```
2. 
```swift
var textZones: [Quadrilateral]? { get set }
```
