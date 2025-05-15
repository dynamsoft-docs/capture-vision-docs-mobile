---
layout: default-layout
title: CapturedResultBase - Dynamsoft Core Module Android Edition API Reference
description: The class CapturedResultBase of Dynamsoft Core Module Android edition is the base class of all types of captured results.
keywords: captured result base, Android
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# CapturedResultBase

The `CapturedResultBase` class is the base class of all types of captured results.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class CapturedResultBase
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash id of the original image. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the [ImageTag](image-tag.md) of the original image. |
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`getErrorCode`](#geterrorcode) | Gets the error code of this result. |
| [`getErrorMessage`](#geterrormessage) | Gets the error message of this result. |

### getOriginalImageHashId

Gets the hash id of the original image.

```java
String getOriginalImageHashId();
```

**Return Value**

The hash id of the original image.

### getOriginalImageTag

Gets the [ImageTag](image-tag.md) of the original image.

```java
ImageTag getOriginalImageTag();
```

**Return Value**

The tag of the original image.

### getRotationTransformMatrix

Gets the rotation transformation matrix of the original image relative to the rotated image.

```java
Matrix getRotationTransformMatrix();
```

**Return Value**

The rotation transformation matrix of the original image relative to the rotated image, of type [Matrix](https://developer.android.com/reference/android/opengl/Matrix){:target="_blank"}.

### getErrorCode

Gets the error code of this result.

```java
int getErrorCode();
```

**Return Value**

The error code of this result.

### getErrorMessage

Gets the error message of this result.

```java
String getErrorMessage();
```

**Return Value**

The error message of this result.
