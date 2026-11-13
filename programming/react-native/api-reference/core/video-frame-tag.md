---
layout: default-layout
title: VideoFrameTag - Dynamsoft Capture Vision React Native
description: Interface VideoFrameTag of Dynamsoft Capture Vision Module React Native edition represents a tag describing an image captured from a video frame.
keywords: video frame tag, image tag, frame quality, React Native
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# VideoFrameTag

Interface `VideoFrameTag` represents a tag describing an image captured from a video frame. It extends [`ImageTag`](image-tag.md).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.6.5000 and Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface VideoFrameTag extends ImageTag
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`quality`](#quality) | [*EnumVideoFrameQuality*](enum/video-frame-quality.md) \| *number* | The quality of the video frame. |
| [`isCropped`](#iscropped) | *boolean* | Whether the video frame is cropped. |
| [`cropRegion`](#cropregion) | [*DSRect*](dsrect.md) \| *null* | The crop region of the video frame. |
| [`originalWidth`](#originalwidth) | *number* | The original width of the video frame. |
| [`originalHeight`](#originalheight) | *number* | The original height of the video frame. |
| [`clarity`](#clarity) | *number* | The clarity of the video frame. |

The following properties are inherited from [`ImageTag`](image-tag.md):

| Properties | Types | Description |
| ---------- | ----- | ----------- |
| [`imageId`](image-tag.md#imageid) | *number* | The ID of the image this tag belongs to. |
| [`tagType`](image-tag.md#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) \| *number* | The type of the tag. Always `ITT_VIDEO_FRAME` for `VideoFrameTag`. |

### quality

The quality of the video frame.

```js
quality: EnumVideoFrameQuality | number;
```

### isCropped

Whether the video frame is cropped.

```js
isCropped: boolean;
```

### cropRegion

The crop region of the video frame.

```js
cropRegion: DSRect | null;
```

### originalWidth

The original width of the video frame.

```js
originalWidth: number;
```

### originalHeight

The original height of the video frame.

```js
originalHeight: number;
```

### clarity

The clarity of the video frame.

```js
clarity: number;
```
