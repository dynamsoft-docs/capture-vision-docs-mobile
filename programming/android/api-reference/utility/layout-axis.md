---
layout: default-layout
title: LayoutAxis - Dynamsoft Capture Vision Android Edition API Reference
description: The class LayoutAxis of Dynamsoft Capture Vision Android edition provides axis configuration for layout analysis.
keywords: layout axis, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAxis

The `LayoutAxis` class provides configuration for a single axis in layout analysis.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LayoutAxis
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`elementCount`](#elementcount) | *int* | Expected number of elements along this axis. Use -1 for auto-detection. |
| [`isStaggered`](#isstaggered) | *boolean* | Whether the layout uses an offset/staggered pattern. |
| [`angle`](#angle) | *int* | Target angle [0, 180]. Use -1 for auto-detection. |
| [`isEqualSpacing`](#isequalspacing) | *boolean* | Force equal gaps between elements. When false, spacing is ignored. |
| [`spacing`](#spacing) | *int* | Spacing between elements along this axis. Use -1 for auto-detection. |
| [`spacingUnit`](#spacingunit) | *int* | Interpretation mode for the spacing value. |

### elementCount

Expected number of elements along this axis. Use -1 for auto-detection.

```java
int elementCount;
```

### isStaggered

Whether the layout uses an offset/staggered pattern.

```java
boolean isStaggered;
```

### angle

Target angle [0, 180]. Use -1 for auto-detection.

```java
int angle;
```

### isEqualSpacing

Force equal gaps between elements. When false, spacing is ignored.

```java
boolean isEqualSpacing;
```

### spacing

Spacing between elements along this axis. Use -1 for auto-detection.

```java
int spacing;
```

### spacingUnit

Interpretation mode for the spacing value.

```java
@EnumMeasureUnit
int spacingUnit;
```
