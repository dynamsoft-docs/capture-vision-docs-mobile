---
layout: default-layout
title: FileImageTag - Dynamsoft Capture Vision MAUI API Reference
description: The FileImageTag class describes an image loaded from a file.
keywords: file image tag, file path, page number, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# FileImageTag

The `FileImageTag` class extends [`ImageTag`](image-tag.md) and describes an image loaded from a file or a page of a PDF file.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public class FileImageTag : ImageTag
```

## Properties & Methods

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`FilePath`](#filepath) | *string?* | The path of the image file. |
| [`PageNumber`](#pagenumber) | *int* | The page number of the current image in the file. |
| [`TotalPages`](#totalpages) | *int* | The total number of pages in the file. |

The following properties are inherited from [`ImageTag`](image-tag.md):

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`ImageId`](image-tag.md#imageid) | *int* | The ID of the image this tag belongs to. |
| [`TagType`](image-tag.md#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) | The tag type, `ITT_FILE_IMAGE`. |

| Method | Description |
| ------ | ----------- |
| [`FileImageTag`](#fileimagetag-1) | Creates a file image tag. |

### FilePath

The path of the image file.

```csharp
public string? FilePath { get; set; }
```

### PageNumber

The page number of the current image in the file.

```csharp
public int PageNumber { get; set; }
```

### TotalPages

The total number of pages in the file.

```csharp
public int TotalPages { get; set; }
```

### FileImageTag

Creates a file image tag. The first overload sets the image ID to `0`.

```csharp
public FileImageTag(string? filePath, int pageNumber, int totalPages);
public FileImageTag(int imageId, string? filePath, int pageNumber, int totalPages);
```

**Parameters**

`imageId`: The ID of the image.

`filePath`: The path of the image file, or `null`.

`pageNumber`: The page number of the current image in the file.

`totalPages`: The total number of pages in the file.
