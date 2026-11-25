---
layout: default-layout
title: VideoFrameTag - Dynamsoft Capture Vision MAUI API Reference
description: The VideoFrameTag class describes an image captured from a video frame.
keywords: video frame tag, frame quality, crop region, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# VideoFrameTag

The `VideoFrameTag` class extends [`ImageTag`](image-tag.md) and describes an image captured from a video frame.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public class VideoFrameTag : ImageTag
```

## Properties & Methods

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`Quality`](#quality) | [*EnumVideoFrameQuality*](enum/video-frame-quality.md) | The quality of the frame. |
| [`IsCropped`](#iscropped) | *bool* | Whether the frame is cropped. |
| [`CropRegion`](#cropregion) | [*DMRect?*](rect.md) | The crop region in pixels. |
| [`OriginalWidth`](#originalwidth) | *int* | The width of the original video frame. |
| [`OriginalHeight`](#originalheight) | *int* | The height of the original video frame. |
| [`Clarity`](#clarity) | *int* | The clarity of the frame. |

The following properties are inherited from [`ImageTag`](image-tag.md):

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`ImageId`](image-tag.md#imageid) | *int* | The ID of the image this tag belongs to. |
| [`TagType`](image-tag.md#tagtype) | [*EnumImageTagType*](enum/image-tag-type.md) | The tag type, `ITT_VIDEO_FRAME`. |

| Method | Description |
| ------ | ----------- |
| [`VideoFrameTag`](#videoframetag-1) | Creates a video frame tag. |

### Quality

The quality of the frame. Its default value is `VFQ_UNKNOWN`.

```csharp
public EnumVideoFrameQuality Quality { get; set; }
```

### IsCropped

Whether the frame is cropped.

```csharp
public bool IsCropped { get; set; }
```

### CropRegion

The crop region in pixels. The `Left`, `Top`, `Right`, and `Bottom` edges of [`DMRect`](rect.md) define the region. `MeasuredInPercentage` is ignored because a crop region is always in pixels. On iOS, the edges are converted to and from a `CGRect` origin and size.

```csharp
public DMRect? CropRegion { get; set; }
```

### OriginalWidth

The width of the original video frame.

```csharp
public int OriginalWidth { get; set; }
```

### OriginalHeight

The height of the original video frame.

```csharp
public int OriginalHeight { get; set; }
```

### Clarity

The clarity of the frame.

```csharp
public int Clarity { get; set; }
```

### VideoFrameTag

Creates a video frame tag. The parameterless constructor sets the image ID to `0` and the quality to `VFQ_UNKNOWN`.

```csharp
public VideoFrameTag();
public VideoFrameTag(int imageId, EnumVideoFrameQuality quality, bool isCropped,
    DMRect? cropRegion, int originalWidth, int originalHeight, int clarity = 0);
```

**Parameters**

`imageId`: The ID of the image.

`quality`: The quality of the frame.

`isCropped`: Whether the frame is cropped.

`cropRegion`: The crop region in pixels, or `null`.

`originalWidth`: The width of the original frame.

`originalHeight`: The height of the original frame.

`clarity`: The clarity of the frame. Defaults to `0`.
