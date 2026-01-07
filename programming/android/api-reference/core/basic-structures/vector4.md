---
layout: default-layout
title: Vector4 - Dynamsoft Capture Vision Android Edition API Reference
description: The class Vector4 of Dynamsoft Capture Vision Android represents a a four-dimensional vector.
keywords: vector4, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Vector4

The `Vector4` class represents a four-dimensional vector.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class Vector4
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`value`](#value) | *int[4]* | The components value of a four-dimensional vector. |

| Methods | Description |
| ------- | ----------- |
| [`Vector4`](#vector4-1) | The constructor. |
| [`Vector4(v1,v2,v3,v4)`](#vector4v1v2v3v4) | Constructs a Vector4 from 4 integer values. |


### value

The components value of a four-dimensional vector.

```java
public int[] value = new int[4];
```

### Vector4

The constructor.

```java
Vector4();
```

### Vector4(v1,v2,v3,v4)

Constructs a Vector4 from 4 integer values.

```java
Vector4(int v1, int v2, int v3, int v4)
```