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

## Attributes

| Method | Description |
| ------ | ----------- |
| [`getLocation`](#getlocation) | Get the location info of the element that defined in Quadrilateral. |
| [`getReferencedElement`](#getreferencedelement) | Get the referenced element that supports the capturing of this element. |
| [`getRegionObjectElementType`](#getregionobjectelementtype) | Get the type of the element. |

### getLocation

Get the location info of the element that defined in Quadrilateral.

```java
Quadrilateral getLocation();
```

### getReferencedElement

Get the referenced element that supports the capturing of this element.

```java
RegionObjectElement getReferencedElement();
```

### getRegionObjectElementType

Get the type of the element.

```java
EnumRegionObjectElementType getType();
```
