---
layout: default-layout
Title: DSIntermediateResultReceiver - Dynamsoft Core Module iOS Edition API Reference
Description: The protocol DSIntermediateResultReceiver includes methods for monitoring the output of intermediate results.
Keywords: protocol, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResultReceiver

The `DSIntermediateResultReceiver` protocol includes methods for monitoring the output of intermediate results.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSIntermediateResultReceiver <NSObject>
```
2. 
```swift
protocol IntermediateResultReceiver: NSObjectProtocol
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getObservationParameters`](#getobservationparameters) | Get a `DSObservationParameters` object to configure the observation settings. |

### getObservationParameters

Get a `DSObservationParameters` object to configure the observation settings.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSObservationParameters *)getObservationParameters;
```
2. 
```swift
```
