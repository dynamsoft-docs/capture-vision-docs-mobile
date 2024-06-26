---
layout: default-layout
title: DSObservationParameters - Dynamsoft Core Module iOS Edition API Reference
description: The class DSObservationParameters of Dynamsoft Core Module represents filter conditions for the DSIntermediateResultReceiver, which allows the user to specify which intermediate results to be notified.
keywords: observation parameters, filter conditions, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSObservationParameters

The `DSObservationParameters` class is used to set filter conditions for the `DSIntermediateResultReceiver`, so that only intermediate results meeting specific conditions will be called back.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSObservationParameters : NSObject
```
2. 
```swift
class ObservationParameters : NSObject
```

## Methods & Attributes

| Method | Description |
|------- |-------------|
| [`addObservedTask`](#addobservedtask) | Adds observed task name to be notified when relevant results are available. |
| [`removeObservedTask`](#removeobservedtask) | Remove the observed task name so that intermediate results generated by the task are not notified. |
| [`isTaskObserved`](#istaskobserved) | Check whether the specified task was observed. |

| Property | Description |
| -------- | ----------- |
| [`resultUnitTypesOnlyForInput`](#resultunittypesonlyforinput) |  |

### addObservedTask

Adds observed task name to be notified when relevant results are available.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)addObservedTask:(NSString *)taskName;
```
2. 
```swift
func addObservedTask(_ taskName: String)
```

**Parameters**

`taskName`: Specify a task name to add to the observation list.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
[observationParameters addObservedTask:@"TextRecognition"];
```
2. 
```swift
observationParameters.addObservedTask("TextRecognition")
```

### removeObservedTask

Remove the observed task name so that intermediate results generated by the task are not notified.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeObservedTask:(NSString*)taskName;
```
2. 
```swift
func removeObservedTask(_ taskName: String)
```

**Parameters**

`taskName`: Specify a task name to remove from the observation list.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
[observationParameters removeObservedTask:@"TextRecognition"];
```
2. 
```swift
observationParameters.removeObservedTask("TextRecognition")
```

### isTaskObserved

Check whether the specified task was observed.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)isTaskObserved:(NSString*)taskName;
```
2. 
```swift
func isTaskObserved(_ taskName: String) -> Bool
```

**Parameters**

`taskName`: Specify a task name to check the observation state.

**Return Value**

A BOOL value that indicates whether the specified task is observed.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
BOOL observed = [observationParameters isTaskObserved:@"TextRecognition"];
```
2. 
```swift
let observed = observationParameters.isTaskObserved("TextRecognition")
```
