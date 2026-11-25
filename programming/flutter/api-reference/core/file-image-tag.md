---
layout: default-layout
title: FileImageTag - Dynamsoft Capture Vision Flutter
description: The FileImageTag class of Dynamsoft Capture Vision Flutter describes an image loaded from a file.
keywords: file image tag, file path, page number, Flutter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# FileImageTag

The `FileImageTag` class extends [`ImageTag`](image-tag.md) and describes an image loaded from a file or a page of a PDF file.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class FileImageTag extends ImageTag {
  String? filePath;
  int pageNumber;
  int totalPages;
}
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`filePath`](#filepath) | *String?* | The path of the image file. |
| [`pageNumber`](#pagenumber) | *int* | The page number of the current image in the file. |
| [`totalPages`](#totalpages) | *int* | The total number of pages in the file. |

The following properties are inherited from [`ImageTag`](image-tag.md):

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`imageId`](image-tag.md#imageid) | *int* | The ID of the image this tag belongs to. |
| [`tagType`](image-tag.md#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) | The tag type, `fileImage`. |

### filePath

The path of the image file.

```dart
String? filePath;
```

### pageNumber

The page number of the current image in the file.

```dart
int pageNumber;
```

### totalPages

The total number of pages in the file.

```dart
int totalPages;
```
