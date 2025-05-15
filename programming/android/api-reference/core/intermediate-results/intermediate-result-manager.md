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

> You are reading a history page of `DynamsoftCore`. Start from v3.2.10, the `IntermediateResultManager` class is moved to the `DynamsoftCaptureVisionRouter` module. View the [`DynamsoftCaptureVisionRouter.IntermediateResultManager`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/intermediate-result-manager.html) for the latest version.

The `IntermediateResultManager` class is responsible for handling intermediate results obtained during the process of an image. It offers methods to both register and deregister receivers of these intermediate results, as well as to retrieve the original image data.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

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

`[in] receiver`: A delegate object of `IntermediateResultReceiver`.  

### removeResultReceiver

Removes the specified `IntermediateResultReceiver` object.

```java
void removeResultReceiver(IntermediateResultReceiver receiver);
```

**Parameters**

`[in] receiver`: A delegate object of [`IntermediateResultReceiver`](intermediate-result-receiver.md).  

### getOriginalImage

Retrieves the original image data.

```java
ImageData getOriginalImage(String imageHashId);
```

**Parameters**

`[in] imageHashId`: The image hash ID.

**Return Value**

The original image data, of type [`ImageData`](../basic-structures/image-data.md).
