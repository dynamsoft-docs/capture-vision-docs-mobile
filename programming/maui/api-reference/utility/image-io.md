---
layout: default-layout
title: DMImageIO - Dynamsoft Capture Vision Router Module MAUI Edition API Reference
description: The class DMImageIO of Dynamsoft Capture Vision MAUI is a utility class that provides functionality for reading and saving images.
keywords: image IO, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DMImageIO

The `DMImageIO` class is a utility class that provides functionality for reading and saving images.

## Definition

*Namespace:* Dynamsoft.Utility.Maui

*Assembly:* Dynamsoft.Utility.Maui

```csharp
class DMImageIO
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`SaveToFile`](#savetofile) | Saves an image to the specified path and format. |
| [`ReadFromFile`](#readfromfile) | Read an image from file with the file path. |

### saveToFile

Saves an image to the specified path and format. The desired file format is inferred from the file extension provided in the `path` parameter.

```csharp
void SaveToFile(ImageData imageData, string path, bool overWrite);
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

### ReadFromFile

Read an image from file with the file path

```csharp
ImageData? ReadFromFile(string path);
```

**Parameters**

`[in] path`: The file path.

**Return Value**

The read image data of type `ImageData`.
