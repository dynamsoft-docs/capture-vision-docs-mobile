---
layout: default-layout
title: ImageTag - Dynamsoft Capture Vision React Native
description: Interface ImageTag of Dynamsoft Capture Vision Module React Native edition represents the tag attached to an image.
keywords: image tag, tag type, React Native
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageTag

Interface `ImageTag` represents the tag attached to an image. It is carried by a [`CapturedResultBase`](captured-result-base.md) as `originalImageTag`.

> [!NOTE]
> Hierarchy:
> - `ImageTag`
>   - [`FileImageTag`](file-image-tag.md)
>   - [`VideoFrameTag`](video-frame-tag.md)

The JSI and event-emitter layers return a plain JavaScript object with concrete tag fields on the same level. Use [`tagType`](#tagtype) to determine which concrete shape the object has, then narrow it to [`FileImageTag`](file-image-tag.md) or [`VideoFrameTag`](video-frame-tag.md).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.6.5000 and Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface ImageTag
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`imageId`](#imageid) | *number* | The ID of the image this tag belongs to. |
| [`tagType`](#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) \| *number* | The type of the tag. |

### imageId

The ID of the image this tag belongs to.

```js
imageId: number;
```

### tagType

The type of the tag. Read-only on the native side.

```js
tagType: EnumImageTagType | number;
```

**See also**

- [`EnumImageTagType`](enum/image-tag-type.md)
