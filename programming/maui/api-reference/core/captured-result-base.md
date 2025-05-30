---
layout: default-layout
title: CapturedResultBase - Dynamsoft Core Module MAUI Edition API Reference
description: The class CapturedResultBase of Dynamsoft Core Module MAUI edition is the base class of all types of captured results.
keywords: captured result base, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# CapturedResultBase

The `CapturedResultBase` class is the base class of all types of captured results.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
class CapturedResultBase
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`OriginalImageHashId`](#originalimagehashid) | *string* | Gets the hash id of the original image. |
| [`RotationTransformMatrix`](#rotationtransformmatrix) | *Matrix* | Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`ErrorCode`](#errorcode) | *int* | Gets the error code of this result. |
| [`ErrorMessage`](#errormessage) | *string* | Gets the error message of this result. |

### getOriginalImageHashId

Gets the hash id of the original image.

```csharp
string OriginalImageHashId { get; }
```

### RotationTransformMatrix

Gets the rotation transformation matrix of the original image relative to the rotated image.

```csharp
Matrix RotationTransformMatrix { get; }
```

### ErrorCode

Gets the error code of this result.

```csharp
int ErrorCode { get; }
```

### ErrorMessage

Gets the error message of this result.

```csharp
String ErrorMessage { get; }
```
