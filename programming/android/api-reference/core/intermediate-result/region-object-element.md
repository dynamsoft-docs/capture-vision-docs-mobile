---
layout: default-layout
Title: DSRegionObjectElement - Dynamsoft Core Module Android Edition API Reference
Description: The class DSRegionObjectElement of Dynamsoft Core Module represents an element of a region object in 2D space, which provides the interface for region object elements.
Keywords: region object element, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRegionObjectElement

The `DSRegionObjectElement` class represents an element of a region object in 2D space, which provides the interface for region object elements.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class RegionObjectElement
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`location`](#location) | *DSQuadrilateral \** | The location info of the element that defined in DSQuadrilateral. |
| [`referencedElement`](#referencedelement) | *DSRegionObjectElement \** | The referenced element that supports the capturing of this element. |
| [`regionObjectElementType`](#regionobjectelementtype) | *DSRegionObjectElementType* | The type of the element. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The transformation matrix that can transfer the points cooridinates from. |

### location

The location info of the element that defined in DSQuadrilateral.

```java
var location: DSQuadrilateral? { get set }
```

### referencedElement

The referenced element that supports the capturing of this element.

```java
var referencedElement: RegionObjectElement? { get }
```

### regionObjectElementType

The type of the element.

```java
var regionObjectElementType: EnumRegionObjectElementType { get }
```

### rotationTransformMatrix

The transformation matrix that can transfer the points cooridinates from.

```java
var rotationTransformMatrix: CGAffineTransform { get }
```
