---
layout: default-layout
Title: CapturedResult - Dynamsoft Core Module Android Edition API Reference
Description: The class CapturedResult of Dynamsoft Core Module represents the result of a capture operation on an image, which contains multiple items such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.
Keywords: captured result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CapturedResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class CapturedResult
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`sourceImageHashId`](#sourceimagehashid) | *NSString \** | The hash id of the source image. You can use this ID to get the source image via `IntermediateResultManager` class. |
| [`sourceImageTag`](#sourceimagetag) | *DSImageTag* | The tag of the source image that records the information of the source image. |
| [`items`](#items) | *NSArray<CapturedResultItem*> \** | An array of `CapturedResultItems`, which are the basic unit of the captured results. A `CapturedResultItem` can be a raw image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View CapturedResultItemType for all available types. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |

### sourceImageHashId

The hash id of the source image. You can use this ID to get the source image via IntermediateResultManager class.

```java
var sourceImageHashId: String { get }
```

### sourceImageTag

The tag of the source image that records the information of the source image.

```java
var sourceImageTag: ImageTag { get }
```

### items

An array of CapturedResultItems, which are the basic unit of the captured results. A CapturedResultItem can be a raw image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View CapturedResultItemType for all available types.

```java
var items: [CapturedResultItem]? { get }
```

### rotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image.

```java
var rotationTransformMatrix: CGAffineTransform { get }
```
