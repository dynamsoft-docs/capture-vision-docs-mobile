---
layout: default-layout
title: CapturedResultBase - Dynamsoft Capture Vision React Native
description: Interface CapturedResultBase of Dynamsoft Capture Vision Module React Native edition is the base interface of all types of captured results.
keywords: captured result base, React Native
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultBase

Interface `CapturedResultBase` is the base interface of all types of captured results.

> [!NOTE]
> Hierarchy:
> - `CapturedResultBase`
>   - [`CapturedResult`](../capture-vision-router/captured-result.md)
>   - [`DecodedBarcodesResult`]({{ site.dbr_react_native_api }}barcode-reader/decoded-barcodes-result.html)
>   - [`RecognizedTextLinesResult`]({{ site.dlr_react_native_api }}recognized-text-lines-result.html)
>   - [`ProcessedDocumentResult`]({{ site.ddn_react_native_api }}processed-document-result.html)
>   - [`ParsedResult`]({{ site.dcp_react_native_api }}parsed-result.html)

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface CapturedResultBase
```

## Properties

| Properties | Types | Description |
| ---------- | ----- | ----------- |
| [`originalImageHashId`](#originalimagehashid) | *string* | The hash id of the original image. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *number[]* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`](#errorcode) | *number* | The error code of this result. |
| [`errorMessage`](#errormessage) | *string* | The error message of this result. |

### originalImageHashId

The hash id of the original image.

```js
originalImageHashId: string;
```

### rotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image.

```js
rotationTransformMatrix: number[];
```

### errorCode

The error code of this result.

```js
errorCode: number;
```

### errorMessage

The error message of this result.

```js
errorMessage: string;
```
