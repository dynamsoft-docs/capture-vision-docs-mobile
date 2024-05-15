---
layout: default-layout
title: DSFileImageTag - Dynamsoft Core Module iOS Edition API Reference
description: The class DSFileImageTag of Dynamsoft Core Module represents an image tag that is associated with a file, which contains the file path, page number, and total page number.
keywords: image tag, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSFileImageTag

The `DSFileImageTag` class represents an image tag that is associated with a file. It inherits from the `DSImageTag` class and adds additional attributes.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSFileImageTag : DSImageTag
```
2. 
```swift
class FileImageTag : ImageTag
```

## Methods & Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`filePath`](#filepath) | *NSString \** | The file path of the image. |
| [`pageNumber`](#pagenumber) | *NSInteger* | The page number of the current image in the file. |
| [`totalPages`](#totalpages) | *NSInteger* | The total page number of the file. |

| Method | Description |
| ------ | ----------- |
| [`initWithImageId`](#initwithimageid) | The constructor of the FileImageTag. |

### filePath

The file path of the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, readonly) NSString *filePath;
```
2. 
```swift
var filePath: String? { get }
```

### pageNumber

The page number of the current image in the multi-page.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) NSInteger pageNumber;
```
2. 
```swift
var pageNumber: Int { get }
```

### totalPages

The total page number of the multi-page.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) NSInteger totalPages;
```
2. 
```swift
var totalPages: Int { get }
```

### initWithImageId

The constructor of the FileImageTag.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithImageId:(NSInteger)imageId
                       filePath:(NSString *)filePath
                     pageNumber:(NSInteger)pageNumber
                     totalPages:(NSInteger)totalPages;
```
2. 
```swift
init(imageId: Int, filePath: String, pageNumber: Int, totalPages: Int)
```

**Parameters**

`imageId`: The ID of the image.  
`filePath`: The file path of the image.  
`pageNumber`: The page number of the current image in the multi-page.  
`totalPages`: The total page number of the multi-page.

**Return Value**

An instance of the `DSFileImageTag`.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DSFileImageTag *fileImageTag = [[DSFileImageTag alloc] initWithImageId:123 filePath:@"Your file path" pageNumber:1 totalPages:10];
```
2. 
```swift
let fileImageTag = DSFileImageTag(imageId: 123, filePath: filePath, pageNumber: 1, totalPages: 10)
```
