---
layout: default-layout
Title: IntermediateResultManager - Dynamsoft Core Module Android Edition API Reference
Description: The class IntermediateResultManager of Dynamsoft Core Module manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get raw image data using an image hash id.
Keywords: intermediate result manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultManager

The `IntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get raw image data using an image hash id.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results
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
void addResultReceiver(IntermediateResultReceiver receiver) throws CoreException;
```

**Parameters**

`receiver`: A delegate object of `IntermediateResultReceiver`.  

**Exception**

An exception is thrown when the result receiver is not added successfully.

**Return Value**

A `BOOL` value that indicates whether the result receiver is added successfully.

### removeResultReceiver

Removes an intermediate result receiver.

```java
void removeResultReceiver(IntermediateResultReceiver receiver) throws CoreException;
```

**Parameters**

`receiver`: A delegate object of `IntermediateResultReceiver`.  

**Exception**

An exception is thrown when the result receiver is not removed successfully.

**Return Value**

A `BOOL` value that indicates whether the result receiver is removed successfully.

### getRawImage

Gets the raw image data using an image hash id.

```java
ImageData getRawImage(String imageHashId);
```

**Parameters**

`imageHashId`: The image hash id.

**Return Value**

The raw image data as `ImageData`.
