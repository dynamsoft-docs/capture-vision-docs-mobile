---
layout: default-layout
title: VideoFrameTag - Dynamsoft Capture Vision Flutter
description: The VideoFrameTag class of Dynamsoft Capture Vision Flutter describes an image captured from a video frame.
keywords: video frame tag, frame quality, crop region, Flutter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# VideoFrameTag

The `VideoFrameTag` class extends [`ImageTag`](image-tag.md) and describes an image captured from a video frame.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class VideoFrameTag extends ImageTag {
  EnumVideoFrameQuality quality;
  bool isCropped;
  DSRect? cropRegion;
  int originalWidth;
  int originalHeight;
  int clarity;
}
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`quality`](#quality) | [*EnumVideoFrameQuality*](enum/video-frame-quality.md) | The quality of the video frame. |
| [`isCropped`](#iscropped) | *bool* | Whether the video frame is cropped. |
| [`cropRegion`](#cropregion) | [*DSRect?*](dsrect.md) | The crop region in pixels. |
| [`originalWidth`](#originalwidth) | *int* | The width of the original uncropped video frame. |
| [`originalHeight`](#originalheight) | *int* | The height of the original uncropped video frame. |
| [`clarity`](#clarity) | *int* | The clarity of the video frame. |

The following properties are inherited from [`ImageTag`](image-tag.md):

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`imageId`](image-tag.md#imageid) | *int* | The ID of the image this tag belongs to. |
| [`tagType`](image-tag.md#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) | The tag type, `videoFrame`. |

### quality

The quality of the video frame.

```dart
EnumVideoFrameQuality quality;
```

### isCropped

Whether the video frame is cropped.

```dart
bool isCropped;
```

### cropRegion

The crop region in pixels, expressed as the four edges of a [`DSRect`](dsrect.md). `measuredInPercentage` is ignored because a crop region is always in pixels.

```dart
DSRect? cropRegion;
```

### originalWidth

The width of the original uncropped video frame.

```dart
int originalWidth;
```

### originalHeight

The height of the original uncropped video frame.

```dart
int originalHeight;
```

### clarity

The clarity of the video frame.

```dart
int clarity;
```
