---
layout: default-layout
title: DSIntermediateResult - Dynamsoft Core Module iOS Edition API Reference
description: The class DSIntermediateResult of Dynamsoft Core Module represents a container containing a collection of DSIntermediateResultUnit objects.
keywords: intermediate result, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResult

The `IntermediateResult` class represents the collection of all intermediate result units produced during image processing.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSIntermediateResult : NSObject
```
2. 
```swift
class IntermediateResult : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`intermediateResultUnits`](#intermediateresultunits) | *NSArray<DSIntermediateResultUnit*>* \** | An array of `DSIntermediateResultUnit` objects, each representing a different type of intermediate result. |

### intermediateResultUnits

An array of `DSIntermediateResultUnit` objects, each representing a different type of intermediate result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nonnull, readonly) NSArray<DSIntermediateResultUnit *> * intermediateResultUnits;
```
2. 
```swift
var intermediateResultUnits: [IntermediateResultUnit] { get }
```
