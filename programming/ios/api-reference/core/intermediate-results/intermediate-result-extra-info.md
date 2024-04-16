---
layout: default-layout
title: DSIntermediateResultExtraInfo - Dynamsoft Core Module iOS Edition API Reference
description: The class DSIntermediateResultExtraInfo of Dynamsoft Core Module represents the extra information for generating an intermediate result unit, which contains the name of the TargetROIDef object, the name of the task object, whether the intermediate result is section-level result, and the type of the section that generates the intermediate result.
keywords: intermediate result extra info, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResultExtraInfo

The `DSIntermediateResultExtraInfo` class represents the extra information for generating an intermediate result unit, which contains the name of the TargetROIDef object, the name of the task object, whether the intermediate result is section-level result, and the type of the section that generates the intermediate result.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSIntermediateResultExtraInfo : NSObject
```
2. 
```swift
class IntermediateResultExtraInfo : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`targetROIDefName`](#targetroidefname) | *NSString \** | The property indicates the name of the `TargetROIDef` object that generated the intermediate result. |
| [`taskName`](#taskname) | *NSString \** | The property indicates the name of the task object that generates the intermediate result. |
| [`isSectionLevelResult`](#issectionlevelresult) | *bool \** | The property indicates whether the result is at the section level. |
| [`sectionType`](#sectiontype) | *[DSSectionType]({{ site.dcv_enumerations }}core/section-type.html?lang=android)* | The property indicates the type of the section that generates the intermediate result. If applicable, as defined by the enumeration `EnumSectionType`. |

### targetROIDefName

The name of the TargetROIDef object that generates the intermediate result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, readonly) NSString *targetROIDefName;
```
2. 
```swift
var targetROIDefName: String { get }
```

### taskName

The name of the task object that generates the intermediate result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, readonly) NSString *taskName;
```
2. 
```swift
var taskName: String { get }
```

### isSectionLevelResult

Whether the intermediate result is section-level result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) bool *isSectionLevelResult;
```
2. 
```swift
var isSectionLevelResult: Bool { get }
```

### sectionType

The type of the section that generates the intermediate result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) DSSectionType sectionType;
```
2. 
```swift
var sectionType: EnumSectionType { get }
```
