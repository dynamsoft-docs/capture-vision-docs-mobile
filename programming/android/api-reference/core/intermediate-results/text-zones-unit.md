---
layout: default-layout
title: TextZonesUnit - Dynamsoft Core Module Android Edition API Reference
description: The class TextZonesUnit of Dynamsoft Core Module represents a unit that contains text zones, which is derived from IntermediateResultUnit class.
keywords: text zones unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextZonesUnit

The `TextZonesUnit` class represents a unit that contains text zones, which is derived from `IntermediateResultUnit` class.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class TextZonesUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getTextZones`](#gettextzones) | Gets the array of `Quadrilaterals` as text zones. |
| [`getCount`](#getcount) | Gets the number of text zones. |
| [`getTextZone`](#gettextzone) | Gets the text zone at the specified index. |
| [`removeAllTextZones`](#removealltextzones) | Removes all text zones. |
| [`removeTextZone`](#removetextzone) | Removes the text zone at the specified index. |
| [`addTextZone`](#addtextzone) | Adds the specified text zone. |
| [`setTextZone`](#settextzone) | Sets the text zone at the specified index. |

### getTextZones

Gets the array of `Quadrilaterals` as text zones.

```java
Quadrilateral[] getTextZones()
```

**Return Value**

The array of `Quadrilaterals` as text zones.

### getCount

Gets the number of text zones.

```java
int getCount()
```

**Return Value**

The number of text zones.

### getTextZone

Gets the text zone at the specified index.

```java
TextZone getTextZone(int index)
```

**Parameters**

`[in] index`: The index of the text zone.

**Return Value**

A `TextZone` object as the text zone at the specified index.

### removeAllTextZones

Removes all text zones.

```java
void removeAllTextZones()
```

### removeTextZone

Removes the text zone at the specified index.

```java
int removeTextZone(int index)
```

**Parameters**

`[in] index`: The index of the text zone.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addTextZone

Adds the specified text zone.

```java
int addTextZone(TextZone textZone, Matrix matrixToOriginalImage)
```

**Parameters**

`[in] textZone`: The text zone to be added.

`[in] matrixToOriginalImage`: The transformation matrix to the original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setTextZone

Sets the text zone at the specified index.

```java
int setTextZone(int index, TextZone textZone, Matrix matrixToOriginalImage)
```

**Parameters**

`[in] index`: The index of the text zone.

`[in] textZone`: The text zone to be set.

`[in] matrixToOriginalImage`: The transformation matrix to the original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
