---
layout: default-layout
title: DSCapturedResultItem - Dynamsoft Core Module iOS Edition API Reference
description: The class DSCapturedResultItem of Dynamsoft Core Module represents an item in a captured result, such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
keywords: captured result item, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCapturedResultItem

The `DSCapturedResultItem` class represents an item in a captured result, such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCapturedResultItem : NSObject
```
2. 
```swift
class CapturedResultItem : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`type`](#type) | *DSCapturedResultItemType* | The type of the captured result item, indicating what kind of data it represents. |
| [`referencedItem`](#referenceditem) | *DSCapturedResultItem \** | A property of type `DSCapturedResultItem` that represents a reference to another captured result item. |
| [`targetROIDefName`](#targetroidefname) | *NSString* | The name of the target ROI definition which includes a task that generated the result. |
| [`taskName`](#taskname) | *NSString* | The name of the task that generated the result. |

### type

The type of the captured result item.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) DSCapturedResultItemType type
```
2. 
```swift
var type: DSCapturedResultItemType { get }
```

### referencedItem

The referenced captured result item. The reference dependencies is defined in the Capture Vision settings.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) DSCapturedResultItem *referencedItem
```
2. 
```swift
var referencedItem: DSCapturedResultItem? { get }
```

### targetROIDefName

The name of the `targetROIDef` that produced this `CapturedResultItem`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSString *targetROIDefName
```
2. 
```swift
var targetROIDefName: String? { get }
```

### taskName

The name of the `Task` that produced this `CapturedResultItem`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSString *taskName
```
2. 
```swift
var taskName: String? { get }
```
