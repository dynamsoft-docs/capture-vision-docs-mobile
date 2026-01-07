---
layout: default-layout
title: BufferedItemsManager - Dynamsoft Capture Vision iOS API Reference
description: The BufferedItemsManager class of DCV iOS edition is used to manage the buffered items.
keywords: buffered items, manager, Objc, Objective-C, Swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BufferedItemsManager

The `BufferedItemsManager` class is used to manage the buffered items.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSBufferedItemsManager : NSObject
```
2. 
```swift
class BufferedItemsManager : NSObject
```

## Methods

| Method | Description |
|------- |-------------|
| [`setMaxBufferedItems`](#setmaxbuffereditems) | Set the maximum number of buffered items. |
| [`getMaxBufferedItems`](#getmaxbuffereditems) | Get the maximum number of buffered items. |
| [`getBufferedCharacterItemSet`](#getbufferedcharacteritemset) | Get the buffered item set. |

### setMaxBufferedItems

Set the maximum number of buffered items.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)setMaxBufferedItems:(NSInteger)maxBufferedItems;
```
2. 
```swift
func setMaxBufferedItems(_ maxBufferedItems: Int)
```

**Parameters**

`[in] count`: The maximum number of buffered items.

### getMaxBufferedItems

Get the maximum number of buffered items.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getMaxBufferedItems;
```
2. 
```swift
func getMaxBufferedItems() -> Int
```

**Return Value**

The maximum number of buffered items.

### getBufferedCharacterItemSet

Get the buffered item set.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(DSBufferedCharacterItemSet *)getBufferedCharacterItemSet;
```
2. 
```swift
func getBufferedCharacterItemSet() -> BufferedCharacterItemSet
```

**Return Value**

The buffered item set.
