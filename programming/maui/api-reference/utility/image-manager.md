---
layout: default-layout
title: ImageManager - Dynamsoft Capture Vision MAUI API Reference
description: The class ImageManager of Dynamsoft Capture Vision MAUI is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.
keywords: image manager, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageManager

The `ImageManager` class is a utility class for managing and manipulating images. It provides functionality for saving images to files and drawing various shapes on images.

## Definition

*Namespace:* Dynamsoft.Utility.Maui

*Assembly:* Dynamsoft.Utility.Maui

```csharp
class ImageManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`SaveToFile`](#savetofile) | Saves an image to the specified path and format. |
| [`DrawOnImage`](#drawonimage) | Add quadrilaterals on the image. |

### saveToFile

Saves an image to the specified path and format. The desired file format is inferred from the file extension provided in the `path` parameter.

```csharp
public void SaveToFile(ImageData imageData, String path, bool overWrite);
```

**Parameters**

`[in] imageData`: The image to be saved, of type `ImageData`.

`[in] path`: The file path, name and extension name, as a string, under which the image will be saved.

`[in] overWrite`: A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**Return Value**

A boolean value that indicates whether the file is saved successfully.

### DrawOnImage

Add quadrilaterals on the image.

```csharp
ImageData DrawOnImage(ImageData imageData, Quadrilateral[] quads, int colour, int thickness);
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.  

`[in] quads`: An array of `Quadrilateral` objects to be added on the image.  

`[in] colour`: An int value as an ARGB colour.  

`[in] thickness`: The width of the border.

**Return Value**

The modified `ImageData`.
