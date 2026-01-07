---
layout: default-layout
title: OriginalImageResultItem - Dynamsoft Capture Vision Android Edition API Reference
description: The class OriginalImageResultItem of Dynamsoft Capture Vision Android represents a captured original image result item, which provides an property to get the image data.
keywords: original image result item, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# OriginalImageResultItem

The `OriginalImageResultItem` class extends the [`CapturedResultItem`](captured-result.md) class and represents an original image result item.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class OriginalImageResultItem extends CapturedResultItem
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Get the image data of the captured original image result item. |

## Inherited Methods

| Method | Description |
| ------ | ----------- |
| [`getType`](captured-result.md#gettype) | Get the type of the captured result item, indicating what kind of data it represents. |
| [`getReferenceItem`](captured-result.md#getreferenceitem) | Get a property of type `CapturedResultItem` that represents a reference to another captured result item. |
| [`getTargetROIDefName`](captured-result.md#gettargetroidefname) | Gets the name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object which includes a task that generated the result. |
| [`getTaskName`](captured-result.md#gettaskname) | The name of the task that generated the result. |

### getImageData

Get the image data of the captured original image result item.

```java
@Nullable
ImageData getImageData();
```

**Return Value**

The image data of the captured original image result item.
