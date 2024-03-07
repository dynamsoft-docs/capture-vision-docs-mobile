---
layout: default-layout
title: DSIntermediateResultManager - Dynamsoft Core Module iOS Edition API Reference
description: The class DSIntermediateResultManager of Dynamsoft Core Module manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.
keywords: intermediate result manager, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResultManager

The `DSIntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSIntermediateResultManager: NSObject
```
2. 
```swift
class IntermediateResultManager : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`addResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes an intermediate result receiver. |
| [`getOriginalImage`](#getoriginalimage) | Gets the original image data using the image's hash ID. |

### addResultReceiver

Adds an intermediate result receiver to an `IntermediateResultManager` object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addResultReceiver:(id<DSIntermediateResultReceiver>)receiver;
```
2. 
```swift
func addResultReceiver(_ receiver: DSIntermediateResultReceiver)
```

**Parameters**

`receiver`: A delegate object of `DSIntermediateResultReceiver`.  

**Return Value**

A `BOOL` value that indicates whether the result receiver is added successfully.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
BOOL result = [resultManager addResultReceiver:receiver];
```
2. 
```swift
resultManager.addResultReceiver(receiver)
```

### removeResultReceiver

Removes an intermediate result receiver from an `IntermediateResultManager` object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeResultReceiver:(id<DSIntermediateResultReceiver>)receiver;
```
2. 
```swift
func removeResultReceiver(_ receiver: DSIntermediateResultReceiver)
```

**Parameters**

`receiver`: A delegate object of [`DSIntermediateResultReceiver`](intermediate-result-receiver.md).

**Return Value**

A `BOOL` value that indicates whether the result receiver is removed successfully.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
result = [resultManager removeResultReceiver:receiver];
```
2. 
```swift
resultManager.removeResultReceiver(receiver)
```

### getOriginalImage

Gets the original image data using the image's hash ID.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData)getOriginalImage:(NSString)imageHashId;
```
2. 
```swift
func getOriginalImage(_ imageHashId: String) -> DSImageData
```

**Parameters**

`imageHashId`: The image hash ID.

**Return Value**

The original image data as [`DSImageData`](../basic-structures/image-data.md).

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DSImageData *imageData = [resultManager getOriginalImage:imageHashId];
```
2. 
```swift
let imageData = resultManager.getOriginalImage(imageHashId)
```
