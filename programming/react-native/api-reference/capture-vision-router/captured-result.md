---
layout: default-layout
title: CapturedResult - Dynamsoft Capture Vision React Native
description: CapturedResult interface of DCV React Native edition represents the result of a capture operation on an image.
keywords: decoded barcode, parsed result, error code, output, captured result, react native, barcode reader
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResult

Interface `CapturedResult` represents the result of a capture operation on an image. Internally, `CapturedResult` stores an array of [`CapturedResultItem`](../core/captured-result-item.md), each of which may be a barcode, text line, detected quad, normalized image, original image, or parsed item depending on the functional product that is used.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface CapturedResult extends CapturedResultBase
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`decodedBarcodesResult`](#decodedbarcodesresult) | [*DecodedBarcodesResult*]({{ site.dbr_react_native_api }}barcode-reader/decoded-barcodes-result.html) | All results of type `barcode` in the `CapturedResult` as a `DecodedBarcodesResult` object. |
| [`items`](#items) | *Array\<CapturedResultItem\>?* | An array of [`CapturedResultItem`](captured-result-item.md) objects. |
| [`parsedResult`](#parsedresult) | [*ParsedResult*]({{ site.dcp_react_native_api }}parsed-result.html) | All results of type `parsedResult` in the `CapturedResult` as a `ParsedResult` object. |
| [`processedDocumentResult`](#processeddocumentresult) | [*ProcessedDocumentResult*]({{ site.ddn_react_native_api }}processed-document-result.html) | All results of type `detectedQuad`, `deskewedImage` and `enhancedImage` in the `CapturedResult` as a `ProcessedDocumentResult` object. |
| [`recognizedTextLinesResult`](#recognizedtextlinesresult) | [*RecognizedTextLinesResult*]({{ site.dlr_react_native_api }}recognized-text-lines-result.html) | All results of type `textLine` in the `CapturedResult` as a `RecognizedTextLinesResult` object. |

The following properties are inherited from [`CapturedResultBase`]({{ site.dcv_react_native_api }}core/captured-result-base.html):

| Properties | Types | Description |
| ---------- | ----- | ----------- |
| [`errorCode`]({{ site.dcv_react_native_api }}core/captured-result-base.html#errorcode) | *number* | The error code of this result. |
| [`errorMessage`]({{ site.dcv_react_native_api }}core/captured-result-base.html#errormessage) | *string* | The error message of this result. |
| [`originalImageHashId`]({{ site.dcv_react_native_api }}core/captured-result-base.html#originalimagehashid) | *string* | The hash id of the original image. |
| [`rotationTransformMatrix`]({{ site.dcv_react_native_api }}core/captured-result-base.html#rotationtransformmatrix) | *Array<number>* | The rotation transformation matrix of the original image relative to the rotated image. |

### decodedBarcodesResult

All results of type `barcode` in the `CapturedResult` as a `DecodedBarcodesResult` object.

```js
decodedBarcodesResult?: DecodedBarcodesResult;
```

### items

An array of [`CapturedResultItem`]({{ site.dcv_react_native_api }}captured-result-item.html) objects.

```js
items?: CapturedResultItem[];
```

### parsedResult

All results of type `parsedResult` in the `CapturedResult` as a `ParsedResult` object.

```js
parsedResult?: ParsedResult;
```

#### processedDocumentResult

All results of type `detectedQuad`, `deskewedImage` and `enhancedImage` in the `CapturedResult` as a `ProcessedDocumentResult` object.

```js
processingDocumentResult?: ProcessedDocumentResult;
```

### recognizedTextLinesResult

All results of type `textLine` in the `CapturedResult` as a `RecognizedTextLinesResult` object.

```js
recognizedTextLinesResult?: RecognizedTextLinesResult;
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
