---
layout: default-layout
Title: DSContoursUnit - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSContoursUnit of Dynamsoft Core Module represents a unit that contains contours as intermediate results.
Keywords: contours unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSContoursUnit

The `DSContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `DSIntermediateResultUnit` class.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSContoursUnit: DSIntermediateResultUnit
```
2. 
```swift
class ContoursUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`contours`](#contours) | *NSArray <DSContour**>* | A array of `DSContour` objects. |

### contours

A array of `DSContour` objects.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable) NSArray<DSContour*>* contours;
```
2. 
```swift
var contours: [Contour]? { get set }
```
