---
layout: default-layout
title: DSNeuralNetworkModule - Dynamsoft Neural Network Module iOS Edition API Reference
description: The class DSNeuralNetworkModule of Dynamsoft Neural Network Module represents general functions of the Neural Network module.
keywords: image processing module, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSNeuralNetworkModule

The `DSNeuralNetworkModule` class defines common functionality in the `DynamsoftNeuralNetwork` module.

## Definition

*Assembly:* DynamsoftNeuralNetwork.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSNeuralNetworkModule : NSObject
```
2. 
```swift
class NeuralNetworkModule : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getVersion`](#getversion) | Get the version of `DynamsoftNeuralNetwork` module. |

### getVersion

Get the version of `DynamsoftNeuralNetwork` module.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (NSString *)getVersion;
```
2. 
```swift
class func getVersion() -> String
```

**Return Value**

The version of `DynamsoftNeuralNetwork` module.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSString *version = [DSNeuralNetworkModule getVersion];
```
2. 
```swift
let version = NeuralNetworkModule.getVersion()
```
