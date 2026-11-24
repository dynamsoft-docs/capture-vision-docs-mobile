---
layout: default-layout
title: ImageTag - Dynamsoft Capture Vision MAUI API Reference
description: The abstract ImageTag class represents a tag attached to an image.
keywords: image tag, image ID, tag type, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageTag

The abstract `ImageTag` class represents a tag attached to an [`ImageData`](image-data.md) object. Its subclasses are [`FileImageTag`](file-image-tag.md) and [`VideoFrameTag`](video-frame-tag.md). A tag is also available on [`CapturedResultBase`](captured-result-base.md#originalimagetag).

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.
- The native `distanceMode` property is not exposed.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public abstract class ImageTag
```

## Properties & Methods

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`ImageId`](#imageid) | *int* | The ID of the image this tag belongs to. |
| [`TagType`](#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) | The type of the tag. |

| Method | Description |
| ------ | ----------- |
| [`ImageTag`](#imagetag-1) | The protected constructor. |

### ImageId

The ID of the image this tag belongs to.

```csharp
public int ImageId { get; set; }
```

### TagType

The type of the tag. It is read-only.

```csharp
public EnumImageTagType TagType { get; }
```

### ImageTag

Initializes the image ID and tag type for a subclass.

```csharp
protected ImageTag(int imageId, EnumImageTagType tagType);
```

**Parameters**

`imageId`: The ID of the image.

`tagType`: The type of the tag.
