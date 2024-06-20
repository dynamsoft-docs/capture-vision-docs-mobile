---
layout: default-layout
title: DMRect - Dynamsoft Capture Vision MAUI API Reference
description: The class DMRect of DCV MAUI represents a rectangle in 2D space, which contains four integer values that specify the top, left, right, and bottom edges of the rectangle.
keywords: rectangle, 2D space, scan region
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DMRect

The `DMRect` class represents a rectangle in 2D space, which contains four integer values that specify the top, left, right, and bottom edges of the rectangle.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
class DMRect
```

## Properties & Methods

| Property | Type | Description |
| ---------- | ---- | ----------- |
| [`Top`](#top) | *float* | The distance between the top of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`Left`](#left) | *float* | The distance between the left of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`Right`](#right) | *float* | The distance between the right of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`Bottom`](#bottom) | *float* | The distance between the bottom of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`MeasuredInPercentage`](#measuredinpercentage) | *bool* | Indicates if the rectangle's measurements are in percentages. |

| Method | Description |
| ------ | ----------- |
| [`DMRect`](#dmrect) | The constructor. |

### Top

The distance between the top of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```csharp
float Top { get; set; }
```

### Left

The distance between the left of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```csharp
float Left { get; set; }
```

### Right

The distance between the right of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```csharp
float Right { get; set; }
```

### Bottom

The distance between the bottom of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```csharp
float Bottom { get; set; }
```

### MeasuredInPercentage

Sets whether to use percentages to measure the region size.

```csharp
bool MeasuredInPercentage { get; set; }
```

### DMRect

The constructor.

```csharp
DMRect(float top, float left, float right, float bottom, bool measuredInPercentage);
```

**Parameters**

`[in] top`: The distance between the top of the rect and the x-axis.

`[in] left`: The distance between the left of the rect and the y-axis.

`[in] right`: The distance between the right of the rect and the y-axis.

`[in] bottom`: The distance between the bottom of the rect and the x-axis.

`[in] measuredInPercentage`: Indicates if the rectangle's measurements are in percentages.
