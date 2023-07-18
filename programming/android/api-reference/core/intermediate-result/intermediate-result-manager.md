---
layout: default-layout
Title: DSIntermediateResultManager - Dynamsoft Core Module Android Edition API Reference
Description: The class DSIntermediateResultManager of Dynamsoft Core Module manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get raw image data using an image hash id.
Keywords: intermediate result manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResultManager

The `DSIntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get raw image data using an image hash id.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class IntermediateResultManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`addResultReceiver`](#addresultreceiver) | Adds an intermediate result receiver. |
| [`removeResultReceiver`](#removeresultreceiver) | Adds an intermediate result receiver. |
| [`getRawImage`](#getrawimage) | Gets the raw image data using an image hash id. |

### addResultReceiver

Adds an intermediate result receiver.

```java
func addResultReceiver(_ receiver: DSIntermediateResultReceiver) throws
```

**Parameters**

`receiver`: A delegate object of `DSIntermediateResultReceiver`.  
`error`: An `NSError` pointer. An error occurs when the result receiver is not added successfully.

**Return Value**

A `BOOL` value that indicates whether the result receiver is added successfully.

### removeResultReceiver

Removes an intermediate result receiver.

```java
func removeResultReceiver(_ receiver: DSIntermediateResultReceiver) throws
```

**Parameters**

`receiver`: A delegate object of `DSIntermediateResultReceiver`.  
`error`: An `NSError` pointer. An error occurs when the result receiver is not removed successfully.

**Return Value**

A `BOOL` value that indicates whether the result receiver is removed successfully.

**Code Snippet**

```java
do {
    try resultManager.removeResultReceiver(receiver)
} catch {
    // Handle the error
}
```

### getRawImage

Gets the raw image data using an image hash id.

```java
func getRawImage(_ imageHashId: String) -> DSImageData
```

**Parameters**

`imageHashId`: The image hash id.

**Return Value**

The raw image data as `DSImageData`.

**Code Snippet**

```java
let imageData = resultManager.getRawImage(imageHashId)
```
