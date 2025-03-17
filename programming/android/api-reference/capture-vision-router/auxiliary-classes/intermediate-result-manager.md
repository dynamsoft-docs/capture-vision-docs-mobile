---
layout: default-layout
title: IntermediateResultManager - Dynamsoft Core Module Android Edition API Reference
description: The class IntermediateResultManager of Dynamsoft Core Module manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.
keywords: intermediate result manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultManager

The `IntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
class IntermediateResultManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`addResultReceiver`](#addresultreceiver) | Adds a `IntermediateResultReceiver` object as the receiver of intermediate results. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes the specified `IntermediateResultReceiver` object. |
| [`getOriginalImage`](#getoriginalimage) | Retrieves the original image data. |

### addResultReceiver

Adds a `IntermediateResultReceiver` object as the receiver of intermediate results.

```java
void addResultReceiver(IntermediateResultReceiver receiver);
```

**Parameters**

`[in] receiver`: An [`IntermediateResultReceiver`](intermediate-result-receiver.md) object.  

### removeResultReceiver

Removes the specified `IntermediateResultReceiver` object.

```java
void removeResultReceiver(IntermediateResultReceiver receiver);
```

**Parameters**

`[in] receiver`: An [`IntermediateResultReceiver`](intermediate-result-receiver.md) object.

### getOriginalImage

Retrieves the original image data.

```java
ImageData getOriginalImage(String imageHashId);
```

**Parameters**

`[in] imageHashId`: The image hash ID.

**Return Value**

The original image data as [`ImageData`]({{ site.dcv_android_api }}core/basic-structures/image-data.html).
