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
| [`contours`](#contours) | *NSArray <DSContour**>* | An array of `DSContour` objects. |
| [`hierarchies`](#hierarchies) | *NSArray <DSVector4**>* | An array of `DSVector4` objects. |

### contours

An array of `DSContour` objects.

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

### hierarchies

The contour hierarchies as an array of `DSVector4` objects.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable) NSArray<DSVector4*>* hierarchies;
```
2. 
```swift
var hierarchies: [Vector4]? { get set }
```
