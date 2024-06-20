---
layout: default-layout
title: CapturedResultItem - Dynamsoft Capture Vision MAUI API Reference
description: The class CapturedResultItem of DCV MAUI represents an item in a captured result, such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
keywords: captured result item, MAUI, C#
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` class provides a common structure for representing different types of captured results. Each specific captured result item type will have its own implementation and additional properties specific to that type.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
class CapturedResultItem
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`Type`](#type) | *[EnumCapturedResultItemType]({{ site.dcv_maui_api }}core/enum/captured-result-item-type.html)* | The type of the captured result item, indicating what kind of data it represents. |
| [`TargetROIDefName`](#targetroidefname) | *string* | The name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/){:target="_blank"} object which includes a task that generated the result. |
| [`TaskName`](#taskname) | *string* | The name of the task that generated the result. |

### Type

The type of the captured result item, indicating what kind of data it represents.

```csharp
EnumCapturedResultItemType Type { get; }
```

### TargetROIDefName

The name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/){:target="_blank"} object which includes a task that generated the result. The name is defined in a `CaptureVisionTemplate`.

```csharp
string TargetROIDefName { get; }
```

### TaskName

The name of the task that generated the result. The name is defined in a `CaptureVisionTemplate`.

```csharp
string TaskName { get; }
```
