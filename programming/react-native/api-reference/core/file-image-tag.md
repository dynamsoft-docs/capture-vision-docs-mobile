---
layout: default-layout
title: FileImageTag - Dynamsoft Capture Vision React Native
description: Interface FileImageTag of Dynamsoft Capture Vision Module React Native edition represents a tag describing an image loaded from a file.
keywords: file image tag, image tag, React Native
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# FileImageTag

Interface `FileImageTag` represents a tag describing an image loaded from a file (or a page of a PDF file). It extends [`ImageTag`](image-tag.md).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.6.5000 and Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface FileImageTag extends ImageTag
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`filePath`](#filepath) | *string* \| *null* | The file path of the image. |
| [`pageNumber`](#pagenumber) | *number* | The page number of the current image in the file. |
| [`totalPages`](#totalpages) | *number* | The total number of pages in the file. |

The following properties are inherited from [`ImageTag`](image-tag.md):

| Properties | Types | Description |
| ---------- | ----- | ----------- |
| [`imageId`](image-tag.md#imageid) | *number* | The ID of the image this tag belongs to. |
| [`tagType`](image-tag.md#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) \| *number* | The type of the tag. Always `ITT_FILE_IMAGE` for `FileImageTag`. |

### filePath

The file path of the image.

```js
filePath?: string | null;
```

### pageNumber

The page number of the current image in the file.

```js
pageNumber: number;
```

### totalPages

The total number of pages in the file.

```js
totalPages: number;
```
