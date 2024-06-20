---
layout: default-layout
title: IntermediateResultManager Class - Dynamsoft Capture Vision MAUI Edition
description: The class IntermediateResultManager of DCV MAUI edition manages intermediate results.
keywords: intermediate result manager, get original image
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultManager

The `IntermediateResultManager` class manages intermediate results generated during data capturing. It provides methods to add and remove intermediate result receivers, as well as to get original image data using an image hash id.

## Definition

*Namespace:* Dynamsoft.CaptureVisionRouter.Maui

*Assembly:* Dynamsoft.CaptureVisionRouter.Maui

```csharp
class IntermediateResultManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`GetOriginalImage`](#getoriginalimage) | Get the original image data. |

### GetOriginalImage

The original image data.

```csharp
ImageData GetOriginalImage(String imageHashId);
```
