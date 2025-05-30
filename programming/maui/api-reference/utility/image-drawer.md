---
layout: default-layout
title: ImageDrawer - Dynamsoft Capture Vision Router Module MAUI Edition API Reference
description: The class ImageDrawer of Dynamsoft Capture Vision MAUI is a utility class that provides functionality for drawing various shapes on images.
keywords: image drawer, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageDrawer

The `ImageDrawer` class is a utility class that provides functionality for drawing various shapes on images.

## Definition

*Namespace:* Dynamsoft.Utility.Maui

*Assembly:* Dynamsoft.Utility.Maui

```csharp
class ImageDrawer
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`DrawOnImage`](#drawonimage) | Add quadrilaterals on the image. |

### DrawOnImage

Add quadrilaterals on the image.

```csharp
ImageData? DrawOnImage(ImageData imageData, Quadrilateral[] quads, Color color, int thickness);
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.  

`[in] quads`: An array of `Quadrilateral` objects to be added on the image.  

`[in] color`: An int value as an ARGB colour.  

`[in] thickness`: The width of the border.

**Return Value**

The modified `ImageData`.
