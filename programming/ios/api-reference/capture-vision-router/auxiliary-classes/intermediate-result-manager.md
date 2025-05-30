---
layout: default-layout
title: DSIntermediateResultManager - Dynamsoft Core Module iOS Edition API Reference
description: The class DSIntermediateResultManager of Dynamsoft Core Module manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.
keywords: intermediate result manager, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# DSIntermediateResultManager

The `DSIntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`addResultReceiver`](#addresultreceiver) | Adds a `DSIntermediateResultReceiver` object as the receiver of intermediate results. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes the specified `DSIntermediateResultReceiver` object. |
| [`getOriginalImage`](#getoriginalimage) | Retrieves the original image data. |

### addResultReceiver

Adds a [DSIntermediateResultReceiver](intermediate-result-receiver.md) object as the receiver of intermediate results.

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

`receiver`: A delegate object of [DSIntermediateResultReceiver](intermediate-result-receiver.md).  

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

Removes the specified [DSIntermediateResultReceiver](intermediate-result-receiver.md) object.

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

Retrieves the original image data.

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

The original image data as [`DSImageData`]({{ site.dcv_ios_api }}core/basic-structures/image-data.html).

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
