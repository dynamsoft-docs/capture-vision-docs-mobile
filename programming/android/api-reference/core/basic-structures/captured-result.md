---
layout: default-layout
title: CapturedResult - Dynamsoft Core Module Android Edition API Reference
description: The class CapturedResult of Dynamsoft Core Module represents the result of a capture operation on an image, which contains multiple items such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
keywords: captured result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CapturedResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, original image, parsed item, etc.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class CapturedResult
```

## Attributes

| Method | Description |
| ------ | ----------- |
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Get the hash id of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Get the [ImageTag](image-tag.md) of the original image that records information such as the image ID of the original image. |
| [`getItems`](#getitems) | Get an array of `CapturedResultItems`, which are the basic unit of the captured results. A `CapturedResultItem` can be a original image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View CapturedResultItemType for all available types. |
| [`getrotationTransformMatrix`](#getrotationtransformmatrix) | Get the  rotation transformation matrix of the original image relative to the rotated image. |
| [`getErrorCode`](#geterrorcode) | Get the error code if an error occurs when processing the image. |
| [`getErrorMessage`](#geterrormessage) | Get the error message if an error occurs when processing the image. |

### getOriginalImageHashId

Get the hash ID of the original image which can be used to get the original image via the [IntermediateResultManager](../intermediate-results/intermediate-result-manager.md) class.

```java
String getOriginalImageHashId();
```

**Return Value**

The hash id of the original image.

### getOriginalImageTag

Get the [ImageTag](image-tag.md) of the original image that records information such as the image ID of the original image.

```java
ImageTag getOriginalImageTag();
```

**Return Value**

The tag of the original image that records the information of the original image.

### getItems

Get an array of [`CapturedResultItem`](captured-result-item.md), which is the basic unit of the captured results. A [`CapturedResultItem`](captured-result-item.md) can be a original image, a decoded barcode, a recognized text, a detected quad, a normalized image, or a parsed result. View [`CapturedResultItemType`]({{site.dcv_enumerations}}core/captured-result-item-type.html) for all available types.

```java
CapturedResultItem[] getItems();
```

**Return Value**

An array containing the [`CapturedResultItem`](captured-result-item.md) objects within the captured result.

### getRotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```java
Matrix getRotationTransformMatrix();
```

**Return Value**

Return the rotation transformation matrix of the original image relative to the rotated image.

### getErrorCode

Get the error code if an error occurs when processing the image.

```java
int getErrorCode();
```

### getErrorMessage

Get the error message if an error occurs when processing the image.

```java
String getErrorMessage();
```
