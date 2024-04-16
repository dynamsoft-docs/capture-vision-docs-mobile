---
layout: default-layout
title: IntermediateResultManager - Dynamsoft Core Module Android Edition API Reference
description: The class IntermediateResultManager of Dynamsoft Core Module manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.
keywords: intermediate result manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# IntermediateResultManager

The `IntermediateResultManager` class is responsible for handling intermediate results obtained during the process of an image. It offers methods to both register and deregister receivers of these intermediate results, as well as to retrieve the original image data.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class IntermediateResultManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`addResultReceiver`](#addresultreceiver) | Adds a `IntermediateResultReceiver` object as the receiver of intermediate results. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes the specified `IntermediateResultReceiver` object. |
| [`getOriginalImage`](#getoriginalimage) | Gets the original image data using an image hash id. |

### addResultReceiver

Adds a `IntermediateResultReceiver` object as the receiver of intermediate results.

```java
void addResultReceiver(IntermediateResultReceiver receiver);
```

**Parameters**

`[in] receiver`: A delegate object of `IntermediateResultReceiver`.  

### removeResultReceiver

Removes an intermediate result receiver from an `IntermediateResultManager` object.

```java
void removeResultReceiver(IntermediateResultReceiver receiver);
```

**Parameters**

`[in] receiver`: A delegate object of [`IntermediateResultReceiver`](intermediate-result-receiver.md).  

### getOriginalImage

Gets the original image data using the image's hash ID.

```java
ImageData getOriginalImage(String imageHashId);
```

**Parameters**

`[in] imageHashId`: The image hash ID.

**Return Value**

The original image data as [`ImageData`](../basic-structures/image-data.md).
