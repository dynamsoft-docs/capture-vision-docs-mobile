---
layout: default-layout
Title: RegionObjectElement - Dynamsoft Core Module Android Edition API Reference
Description: The class RegionObjectElement of Dynamsoft Core Module represents an element of a region object in 2D space, which provides the interface for region object elements.
Keywords: region object element, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RegionObjectElement

The `RegionObjectElement` class represents an element of a region object in 2D space, which provides the interface for region object elements.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results
*Assembly:* DynamsoftCore.aar

```java
class RegionObjectElement
```

## Method

| Method | Description |
| ------ | ----------- |
| [`getLocation`](#getlocation) | Gets the location info of the element that defined in Quadrilateral. |
| [`getReferencedElement`](#getreferencedelement) | Gets the referenced element that supports the capturing of this element. |
| [`getRegionObjectElementType`](#getregionobjectelementtype) | Gets the type of the element. |

### getLocation

Gets the location info of the element that defined in Quadrilateral.

```java
Quadrilateral getLocation();
```

**Return Value**

The location info of the element that defined in Quadrilateral.

### getReferencedElement

Gets the referenced element that supports the capturing of this element.

```java
RegionObjectElement getReferencedElement();
```

**Return Value**

The referenced element that supports the capturing of this element.

### getRegionObjectElementType

Gets the type of the element.

```java
EnumRegionObjectElementType getType();
```

**Return Value**

The [`EnumRegionObjectElementType`]({{site.enums}}core/region-object-element-type.html) of the element.
