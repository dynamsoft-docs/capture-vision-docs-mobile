---
layout: default-layout
Title: IntermediateResultManager - Dynamsoft Core Module Android Edition API Reference
Description: The class IntermediateResultManager of Dynamsoft Core Module manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.
Keywords: intermediate result manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultManager

The `IntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

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
| [`getOriginalImage`](#getoriginalimage) | Gets the original image data using an image hash id. |

### addResultReceiver

Adds an intermediate result receiver.

```java
void addResultReceiver(IntermediateResultReceiver receiver);
```

**Parameters**

`[in] receiver`: A delegate object of `IntermediateResultReceiver`.  

**Exception**

An exception is thrown when the result receiver is not added successfully.

### removeResultReceiver

Removes an intermediate result receiver.

```java
void removeResultReceiver(IntermediateResultReceiver receiver);
```

**Parameters**

`[in] receiver`: A delegate object of `IntermediateResultReceiver`.  

**Exception**

An exception is thrown when the result receiver is not removed successfully.

### getOriginalImage

Gets the original image data using an image hash id.

```java
ImageData getOriginalImage(String imageHashId);
```

**Parameters**

`[in] imageHashId`: The image hash id.

**Return Value**

The original image data as `ImageData`.
