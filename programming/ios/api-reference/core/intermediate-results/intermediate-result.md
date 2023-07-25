---
layout: default-layout
Title: DSIntermediateResult - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSIntermediateResult of Dynamsoft Core Module represents a container containing a collection of DSIntermediateResultUnit objects.
Keywords: intermediate result, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResult

The `DSIntermediateResult` class represents a container containing a collection of `DSIntermediateResultUnit` objects.

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
| [`intermediateResultUnits`](#intermediateresultunits) | *NSArray<DSIntermediateResultUnit*>* \** | An array of `DSIntermediateResultUnit` objects. |

### intermediateResultUnits

An array of `DSIntermediateResultUnit` objects.

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
