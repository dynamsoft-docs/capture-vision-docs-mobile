---
layout: default-layout
Title: ContoursUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class ContoursUnit of Dynamsoft Core Module represents a unit that contains contours as intermediate results.
Keywords: contours unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ContoursUnit

The `ContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class ContoursUnit: IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getContours`](#getcontours) | Gets the array of `Contour` objects. |
| [`getHierarchies`](#gethierarchies) | Gets the contour hierarchies as an array of `Vector4` objects. |

### getContours

Gets the array of `Contour` objects.

```java
Contour[] getContours()
```

**Return Value**

The array of `Contour` objects.

### getHierarchies

Gets the contour hierarchies as an array of `Vector4` objects.

```java
Vector4[] getHierarchies()
```

**Return Value**

The contour hierarchies as an array of `Vector4` objects.
