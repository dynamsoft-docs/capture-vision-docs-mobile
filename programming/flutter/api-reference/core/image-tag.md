---
layout: default-layout
title: ImageTag - Dynamsoft Capture Vision Flutter
description: The ImageTag class of Dynamsoft Capture Vision Flutter represents a tag attached to an image.
keywords: image tag, image ID, tag type, Flutter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageTag

The abstract `ImageTag` class represents a tag attached to an image. It is available through [`ImageData.imageTag`](image-data.md#imagetag) and [`CapturedResultBase.originalImageTag`](captured-result-base.md#originalimagetag).

Its concrete subclasses are [`FileImageTag`](file-image-tag.md) and [`VideoFrameTag`](video-frame-tag.md).

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
abstract class ImageTag {
  int imageId;
  final EnumImageTagType tagType;
}
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`imageId`](#imageid) | *int* | The ID of the image this tag belongs to. |
| [`tagType`](#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) | The type of the tag. |

### imageId

The ID of the image this tag belongs to.

```dart
int imageId;
```

### tagType

The type of the tag. It is read-only.

```dart
final EnumImageTagType tagType;
```
