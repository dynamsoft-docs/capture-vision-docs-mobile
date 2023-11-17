---
layout: default-layout
title: DSDirectoryFetcher - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSDirectoryFetcher of Dynamsoft Capture Vision Router Module is a utility class that retrieves a list of files from a specified directory based on certain criteria.
keywords: directory fetcher, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSDirectoryFetcher

> You are viewing a history document page of DynamsoftUtility v1.0.10.

The `DSDirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `DSImageSourceAdapter` class.

## Definition

*Assembly:* DynamsoftUtility.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(DirectoryFetcher)
@interface DSDirectoryFetcher : DSImageSourceAdapter
```
2. 
```swift
class DirectoryFetcher : ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`init`](#init) | Create an instance of DSDirectoryFetcher. |
| [`setDirectory`](#setdirectory) | Sets the directory path and filter for the file search. |
| [`setPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters for reading PDF files. |

### init

Create an instance of DSDirectoryFetcher.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)init;
```
2. 
```swift
init()
```

**Return Value**

An instance of `DSDirectoryFetcher`.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DSDirectoryFetcher *fetcher = [[DSDirectoryFetcher alloc] init];
```
2. 
```swift
let fetcher = DirectoryFetcher()
```

### setDirectory

Sets the directory path and filter for the file search.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)setDirectory:(NSString *)directoryPath
                filter:(nullable NSString *)filter
                recursive:(BOOL)recursive
                error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func setDirectory(_ directoryPath: String, filter: String?, recursive: Bool) throws
```

**Parameters**

`directoryPath`: The directory path.

`filter`: A string that specifies file extensions. It determines which kinds of files to read. e.g ".BMP;.JPG;.GIF".

`recursive`: Specifies whether to load files recursively.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_READ_DIRECTORY_FAILED | -10064 | Failed to read the directory. |

**Return Value**

A `BOOL` value that indicates whether the directory is set successfully.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSError *error;
BOOL success = [fetcher setDirectory:directoryPath filter:nil recursive:YES error:&error];
```
2. 
```swift
do {
   try fetcher.setDirectory(directoryPath, filter: nil, recursive: true)
} catch {
   // Add your code to deal with exceptions.
}
```

### setPDFReadingParameter

Sets the parameters for reading PDF files.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)setPDFReadingParameter:(DSPDFReadingParameter*)para
                    error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func setPDFReadingParameter(_ para: DSPDFReadingParameter) throws
```

**Parameters**

`para`: A `DSPDFReadingParameter` object.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |

**Return Value**

A `BOOL` value that indicates whether the PDF reading mode is set successfully.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSError *error;
BOOL success = [fetcher setPDFReadingParameter:pdfParameter error:&error];
```
2. 
```swift
do {
   try fetcher.setPDFReadingParameter(pdfParameter)
} catch {
   // Add your code to deal with exceptions.
}
```
