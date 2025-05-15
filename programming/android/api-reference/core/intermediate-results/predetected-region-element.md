---
layout: default-layout
title: PredetectedRegionElement - Dynamsoft Core Module Android Edition API Reference
description: The class PredetectedRegionElement of Dynamsoft Core Module represents a pre-detected region element, which is a subclass of RegionObjectElement.
keywords: pre-detected region element, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PredetectedRegionElement

The `PredetectedRegionElement` class represents a pre-detected region element, which is a subclass of `RegionObjectElement`.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class PredetectedRegionElement extends RegionObjectElement
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getModeName`](#getmodename) | Gets the name of the detection mode used to detect this region element. |
| [`setLocation`](#setlocation) | Sets the location of the pre-detected region object. |
| [`getLabelId`](#getlabelid) | Gets the label ID of the pre-detected region object. |
| [`getLabelName`](#getlabelname) | Gets the label name of the pre-detected region object. |

### getModeName

Gets the name of the detection mode used to detect this region element.

```java
String getModeName()
```

**Return Value**

The name of the detection mode used to detect this region element. It can be one of the following:

- "RPM_AUTO"
- "RPM_GENERAL"
- "RPM_GENERAL_RGB_CONTRAST"
- "RPM_GENERAL_GRAY_CONTRAST"
- "RPM_GENERAL_HSV_CONTRAST"

### setLocation

Sets the location of the pre-detected region object.

```java
void setLocation(Quadrilateral location);
```

**Parameters**

`location`: The location info of the element that defined in DSQuadrilateral.

**Return Value**

The location info of the element that defined in DSQuadrilateral.

### getLabelId

Gets the label ID of this pre-detected region.

```java
String getLabelId();
```

**Return Value**

The label ID of this pre-detected region.

### getLabelName

Gets the label name of this pre-detected region element.

```java
String getLabelName();
```

**Return Value**

The label name of this pre-detected region element.
