---
layout: default-layout
Title: DSImageData - Dynamsoft Core Module Android Edition API Reference
Description: The class DSImageData of Dynamsoft Core Module represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.
Keywords: image data, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageData

The `DSImageData` class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class ImageData
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`bytes`](#bytes) | *NSData \** | The image data content in a byte array. |
| [`width`](#width) | *NSInteger* | The width of the image in pixels. |
| [`height`](#height) | *NSInteger* | The height of the image in pixels. |
| [`stride`](#stride) | *NSInteger* | The stride (or scan width) of the image. |
| [`format`](#format) | *DSImagePixelFormat* | The image pixel format used in the image byte array. |
| [`orientation`](#orientation) | *NSInteger* | The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file. |
| [`tag`](#tag) | *DSImageTag \** | The tag of the image. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`toUIImage`](#touiimage) | Transform the DSImageData to a UIImage. |

### bytes

The image data content in a byte array.

```java
var bytes: Data? { get set }
```

## width

The width of the image in pixels.  

```java
var width: Int { get set }
```

## height

The height of the image in pixels.  

```java
var height: Int { get set }
```

## stride

The stride (or scan width) of the image.

```java
var stride: Int { get set }
```

## format

The image pixel format used in the image byte array.

```java
var format: DSImagePixelFormat { get set }
```

## orientation

The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file.

```java
var orientation: Int { get set }
```

## tag

The tag of the image.

```java
var tag?: DSImageTag { get set }
```

## toUIImage

Transform the DSImageData to a UIImage.

```java
func toUIImage() throws -> UIImage
```

**Parameters**

`[in,out] error`: An NSError pointer. An error occurs when the BPP (bit per pixel) is not supported.

**Return Value**

An `UIImage` that converted from the `DSImageData`.
