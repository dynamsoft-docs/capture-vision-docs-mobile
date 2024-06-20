---
layout: default-layout
title: CapturedResultReceiver Interface - Dynamsoft Capture Vision MAUI Edition
description: CapturedResultReceiver interface of DCV MAUI edition is designed as a standardized way for retrieving captured results.
keywords: decoded barcodes, parsed results, captured results, CRR, result receiver, output
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultReceiver

The `CapturedResultReceiver` interface is designed as a standardized way for retrieving captured results in the Dynamsoft Capture Vision architecture. By implementing the `CapturedResultReceiver`, you will receive the callback of the various types of captured results, such as original image, decoded barcode, recognized text line, detected quad, normalized image, or parsed data. The `CapturedResultReceiver` can add a receiver for any type of captured result or for a specific type of captured result, based on the method that is implemented.

## Definition

*Namespace:* Dynamsoft.CaptureVisionRouter.Maui

*Assembly:* Dynamsoft.CaptureVisionRouter.Maui

```csharp
interface ICapturedResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`OnCapturedResultReceived`](#oncapturedresultreceived) | The callback triggered when a generic captured result is available, occurring each time an image finishes its processing. |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The callback triggered when decoded barcodes are available, occurring each time an image finishes its processing. |
| [`OnParsedResultsReceived`](#onparsedresultsreceived) | The callback triggered when parsed results are available, occurring each time an image finishes its processing. |

### OnCapturedResultReceived

The callback method triggered when a generic captured result is available, occurring each time an image finishes its processing. This callback can be used for any result that does not fit into the specific categories of the other callbacks.

```csharp
void OnCapturedResultReceived(CapturedResult result);
```

**Parameters**

`[in] result`: The captured result, an instance of [`CapturedResult`](captured-result.md).

### OnDecodedBarcodesReceived

The callback triggered when decoded barcodes are available, occurring each time an image finishes its processing. This callback is used to handle barcodes that have been successfully decoded by Dynamsoft Barcode Reader

```csharp
void OnDecodedBarcodesReceived(DecodedBarcodesResult result);
```

**Parameters**

`[in] result`: The decoded barcode result, an instance of `DecodedBarcodesResult`.

### OnParsedResultsReceived

The callback triggered when parsed results are available, occurring each time an image finishes its processing. This callback is used for handling results that have been parsed into a structured format by Dynamsoft Code Parser.

```csharp
void OnParsedResultsReceived(ParsedResult result);
```

**Parameters**

`[in] result`: The parsed result, an instance of [`ParsedResult`]({{site.dcp_maui_api}}parsed-result.html).
