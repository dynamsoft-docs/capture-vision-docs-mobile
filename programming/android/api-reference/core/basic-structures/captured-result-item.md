---
layout: default-layout
title: CapturedResultItem - Dynamsoft Core Module Android Edition API Reference
description: The class CapturedResultItem of Dynamsoft Core Module represents an item in a captured result, such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
keywords: captured result item, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` class provides a common structure for representing different types of captured results. Each specific captured result item type will have its own implementation and additional properties specific to that type.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class CapturedResultItem
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getType`](#gettype) | Get the type of the captured result item, indicating what kind of data it represents. |
| [`getReferenceItem`](#getreferenceitem) | Get a property of type `CapturedResultItem` that represents a reference to another captured result item. |
| [`getTargetROIDefName`](#gettargetroidefname) | Gets the name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object which includes a task that generated the result. |
| [`getTaskName`](#gettaskname) | The name of the task that generated the result. |

### getType

Get the type of the captured result item, indicating what kind of data it represents.

```java
EnumCapturedResultItemType getType();
```

**Return Value**

The type of the captured result item.

### getReferenceItem

Get a property of type `CapturedResultItem` that represents a reference to another captured result item.

```java
CapturedResultItem getReferenceItem();
```

**Return Value**

The referenced captured result item.

### getTargetROIDefName

Gets the name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object which includes a task that generated the result.

```java
String getTargetROIDefName();
```

**Return Value**

The name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object.

### getTaskName

The name of the task that generated the result.

```java
String getTaskName();
```

**Return Value**

The name of the task.
