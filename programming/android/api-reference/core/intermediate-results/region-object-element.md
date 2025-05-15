---
layout: default-layout
title: RegionObjectElement - Dynamsoft Core Module Android Edition API Reference
description: The class RegionObjectElement of Dynamsoft Core Module represents an element of a region object in 2D space, which provides the interface for region object elements.
keywords: region object element, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RegionObjectElement

The `RegionObjectElement` class represents a basic element of a region object, including its type, location and reference to another element.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class RegionObjectElement
```

## Method

| Method | Description |
| ------ | ----------- |
| [`getLocation`](#getlocation) | Gets the location of the region object, represented as a [`Quadrilateral`](../basic-structures/quadrilateral.md). |
| [`setLocation`](#setlocation) | Sets the location of the region object, represented as a [`Quadrilateral`](../basic-structures/quadrilateral.md). |
| [`getReferencedElement`](#getreferencedelement) | Gets the referenced element that supports the capturing of this element. |
| [`getRegionObjectElementType`](#getregionobjectelementtype) | The type of the region object element, defined by the enumeration `EnumRegionObjectElementType`. |
| [`getImageData`](#getimagedata) | Gets the image data of this region object element. |

### getLocation

Gets the location of the region object, represented as a [`Quadrilateral`](../basic-structures/quadrilateral.md).

```java
Quadrilateral getLocation();
```

**Return Value**

The location of the region object, represented as a [`Quadrilateral`](../basic-structures/quadrilateral.md).

### setLocation

Sets the location of the region object, represented as a [`Quadrilateral`](../basic-structures/quadrilateral.md).

```java
void setLocation(Quadrilateral location);
```

**Parameters**

`[in] location`: A `Quadrilateral` object that defines the location of the region object.

### getReferencedElement

Gets the referenced element that supports the capturing of this element.

```java
RegionObjectElement getReferencedElement();
```

**Return Value**

The referenced element that supports the capturing of this element.

### getRegionObjectElementType

Gets the type of the region object element, defined by the enumeration [`EnumRegionObjectElementType`]({{site.dcv_enumerations}}core/region-object-element-type.html).

```java
EnumRegionObjectElementType getType();
```

**Return Value**

The type of the region object element.

### getImageData

Gets the image data of this region object element.

```java
ImageData getImageData();
```

**Return Value**

The image data of this region object element.
