---
layout: default-layout
title: EnumPresetTemplate - Dynamsoft Capture Vision Router Lite Flutter
description: The enumeration PresetTemplate of Dynamsoft Capture Vision Router describes the preset template.
keywords: CaptureVisionTemplate, EnumPresetTemplate, single barcode template, speed first, read-rate first, template, preset
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: EnumPresetTemplate
---

# EnumPresetTemplate

`EnumPresetTemplate` is an enumeration of preset templates that are configured for different recognition tasks, depending on the functional product as well as the desired performance from that functional product. These strings can be used when specifying template name with the [`startCapturing`](../../capture-vision-router/capture-vision-router.md#startcapturing) or [`capture`](../../capture-vision-router/capture-vision-router.md#capture) methods of the [`CaptureVisionRouter`](../../capture-vision-router/capture-vision-router.md).

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
static class EnumPresetTemplate {
  static const defaultTemplate = 'Default';
  static const readBarcodes = 'ReadBarcodes_Default';
  static const recognizeTextLines = 'RecognizeTextLines_Default';
  static const detectDocumentBoundaries = 'DetectDocumentBoundaries_Default';
  static const detectAndNormalizeDocument = 'DetectAndNormalizeDocument_Default';
  static const normalizeDocument = 'NormalizeDocument_Default';
  static const readBarcodesSpeedFirst = 'ReadBarcodes_SpeedFirst';
  static const readBarcodesReadRateFirst = 'ReadBarcodes_ReadRateFirst';
  static const readSingleBarcode = 'ReadSingleBarcode';
  static const recognizeNumbers = 'RecognizeNumbers';
  static const recognizeLetters = 'RecognizeLetters';
  static const recognizeNumbersAndLetters = 'RecognizeNumbersAndLetters';
  static const recognizeNumbersAndUppercaseLetters = 'RecognizeNumbersAndUppercaseLetters';
  static const recognizeUppercaseLetters = 'RecognizeUppercaseLetters';
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `defaultTemplate` | The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "Default". |
| `readBarcodes` | The default template for the Barcode Reader that offers a balance between speed and read rate. |
| `readBarcodesSpeedFirst` | The speed first template prioritizes speed over read rate when reading barcodes. |
| `readBarcodesReadRateFirst` | The read rate first template prioritizes read rate over speed when reading barcodes. |
| `readSingleBarcode` | The single barcode template focuses on the single-scan barcode reading mode and should not be used when reading multiple barcodes at a time as it is more speed focused. |
| `recognizeTextLines` | The default template for the Text Line Recognizer. |
| `detectDocumentBoundaries` | The default template for the Document Boundary Detector. |
| `detectAndNormalizeDocument` | The default template for the Document Normalizer. |
| `normalizeDocument` | The default template for the Document Normalizer. |
| `recognizeNumbers` | The default template for the Number Recognizer. |
| `recognizeLetters` | The default template for the Letter Recognizer. |
| `recognizeNumbersAndLetters` | The default template for the Number and Letter Recognizer. |
| `recognizeNumbersAndUppercaseLetters` | The default template for the Number and Uppercase Letter Recognizer. |
| `recognizeUppercaseLetters` | The default template for the Uppercase Letter Recognizer. |
