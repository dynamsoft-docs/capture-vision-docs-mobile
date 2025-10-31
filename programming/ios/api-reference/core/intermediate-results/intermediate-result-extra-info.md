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

The `IntermediateResultExtraInfo` class represents the extra information associated with an intermediate result. It includes properties such as the target ROI definition name, task name, section level result indicator, and section type.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`targetROIDefName`](#targetroidefname) | *NSString \** | The name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object that generates the intermediate result. |
| [`taskName`](#taskname) | *NSString \** | The property indicates the name of the processing task to which this result belongs. |
| [`isSectionLevelResult`](#issectionlevelresult) | *bool \** | The property indicates whether the result is at the section level. |
| [`sectionType`](#sectiontype) | *[DSSectionType]({{ site.dcv_ios_api }}core/enum/section-type.html?lang=objc,swift)* | The property indicates the type of section that generates the result, if applicable, as defined by the enumeration `DSSectionType`. |

### targetROIDefName

The name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object that generates the intermediate result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, copy) NSString *targetROIDefName;
```
2. 
```swift
var targetROIDefName: String { get }
```

### taskName

The name of the processing task to which this result belongs.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, copy) NSString *taskName;
```
2. 
```swift
var taskName: String { get }
```

### isSectionLevelResult

The property indicates whether the result is at the section level.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, assign) BOOL isSectionLevelResult;
```
2. 
```swift
var isSectionLevelResult: Bool { get }
```

### sectionType

The type of section that generates the result, if applicable, as defined by the enumeration `DSSectionType`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, assign) DSSectionType sectionType;
```
2. 
```swift
var sectionType: SectionType { get }
```
