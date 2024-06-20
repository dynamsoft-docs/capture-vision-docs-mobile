---
layout: default-layout
title: ImageSourceAdapter - Dynamsoft Capture Vision MAUI API Reference
description: The class ImageSourceAdapter of DCV MAUI represents an interface for fetching and buffering images.
keywords: image source adapter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceAdapter

The `ImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
class ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`StartFetching`](#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`StopFetching`](#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`SetMaximumImageCount`](#setmaximumimagecount) | Sets the maximum number of images that can be buffered at any time. |
| [`GetMaximumImageCount`](#getmaximumimagecount) | Returns the maximum number of images that can be buffered. |
| [`GetImageCount`](#getimagecount) | Returns the current number of images in the buffer. |
| [`IsBufferEmpty`](#isbufferempty) | Determines whether the buffer is currently empty. |
| [`ClearBuffer`](#clearbuffer) | Clears all images from the buffer, resetting the state for new image fetching. |
| [`SetColourChannelUsageType`](#setcolourchannelusagetype) | Sets the usage type for color channels in images. |
| [`GetColourChannelUsageType`](#getcolourchannelusagetype) | Returns the current usage type for color channels in images. |

### StartFetching

Start fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```csharp
void StartFetching();
```

### StopFetching

Stop fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```csharp
void StopFetching();
```

### SetMaximumImageCount

Sets the maximum number of images that can be buffered at any time.

```csharp
void SetMaximumImageCount(int count);
```

**Parameters**

`[in] count`: The maximum capability of the Video Buffer.

### GetMaximumImageCount

Get the maximum number of images that can be buffered.

```csharp
int GetMaximumImageCount();
```

**Return Value**

The maximum capability of the Video Buffer.

### GetImageCount

Get the current number of images in the buffer.

```csharp
int GetImageCount();
```

**Return Value**

The current number of images in the buffer.

### IsBufferEmpty

Determines whether the buffer is currently empty.

```csharp
bool IsBufferEmpty();
```

**Return Value**

A boolean value that indicates whether the Video Buffer is empty.

### ClearBuffer

Clears all images from the buffer, resetting the state for new image fetching.

```csharp
void ClearBuffer();
```

### SetColourChannelUsageType

Sets the usage type for color channels in images.

```csharp
void SetColourChannelUsageType(EnumColourChannelUsageType type);
```

**Parameters**

`[in] type`: One of the [`EnumColourChannelUsageType`]({{site.dcv_maui_api}}core/enum/colour-channel-usage-type.html) that indicates whether the colour channel usage type.

**Return Value**

One of the [`EnumColourChannelUsageType`]({{site.dcv_maui_api}}core/enum/colour-channel-usage-type.html) that indicates whether the colour channel usage type.

### GetColourChannelUsageType

Get the current usage type for color channels in images.

```csharp
EnumColourChannelUsageType GetColourChannelUsageType();
```

**Return Value**

A [`EnumColourChannelUsageType`]({{site.dcv_maui_api}}core/enum/colour-channel-usage-type.html) value that indicates whether the colour channel usage type.
