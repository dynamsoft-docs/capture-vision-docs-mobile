---
layout: default-layout
Title: DSQuadrilateral - Dynamsoft Core Module Android Edition API Reference
Description: The class DSQuadrilateral of Dynamsoft Core Module represents a quadrilateral shape in 2D space, which contains an array of four CGPoint, representing the vertices of the quadrilateral.
Keywords: quadrilateral, shape, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSQuadrilateral

The `DSQuadrilateral` class represents a quadrilateral shape in 2D space, which contains an array of four CGPoint, representing the vertices of the quadrilateral.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class Quadrilateral
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *NSArray* |Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`contains`](#contains) | Check whether the input point is contained by the quadrilateral. |
| [`getBoundingRect`](#getboundingrect) | Get the bounding rectangle of the quadrilateral. |
| [`getCentrePoint`](#getcentrepoint) | Get the centre point of the quadrilateral. |
| [`getArea`](#getarea) | Get the area of the quadrilateral. |

### points

Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex.

```java
var points: [CGPoint] { get set }
```

## contains

Check whether the input point is contained by the quadrilateral.

```java
func contains(_ point: CGPoint) -> Bool
```

**Parameters**

`point`: Input a point.

**Return Value**

A `BOOL` value that indicates whether the point is contained by the quadrilateral.

**Code Snippet**

```java
let result = quadrilateral.contains(point)
```

## getBoundingRect

Get the bounding rectangle of the quadrilateral.

```java
func getBoundingRect() -> CGRect
```

**Return Value**

The bounding rectangle of the quadrilateral.

**Code Snippet**

```java
let rect = quadrilateral.getBoundingRect()
```

## getCentrePoint

Get the centre point of the quadrilateral.

```java
func getCentrePoint() -> CGPoint
```

**Return Value**

The centre point of the quadrilateral.

**Code Snippet**

```java
let center = quadrilateral.getCentrePoint()
```

## getArea

Get the area of the quadrilateral.

```java
func getArea() -> Int
```

**Return Value**

The area of the quadrilateral.

**Code Snippet**

```java
let area = quadrilateral.getArea()
```
