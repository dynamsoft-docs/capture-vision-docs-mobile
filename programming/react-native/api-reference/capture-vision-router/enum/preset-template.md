---
layout: default-layout
title: EnumPresetTemplate - Dynamsoft Capture Vision Router Lite React Native
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

*Assembly:* dynamsoft-barcode-reader-bundle-react-native

```js
enum EnumPresetTemplate {
    PT_DEFAULT = "Default",
    PT_READ_BARCODES = "ReadBarcodes_Default",
    PT_RECOGNIZE_TEXT_LINES = "RecognizeTextLines_Default",
    PT_DETECT_DOCUMENT_BOUNDARIES = "DetectDocumentBoundaries_Default",
    PT_DETECT_AND_NORMALIZE_DOCUMENT = "DetectAndNormalizeDocument_Default",
    PT_NORMALIZE_DOCUMENT = "NormalizeDocument_Default",
    PT_READ_BARCODES_SPEED_FIRST = "ReadBarcodes_SpeedFirst",
    PT_READ_BARCODES_READ_RATE_FIRST = "ReadBarcodes_ReadRateFirst",
    PT_READ_SINGLE_BARCODE = "ReadSingleBarcode",
    PT_RECOGNIZE_NUMBERS = "RecognizeNumbers",
    PT_RECOGNIZE_LETTERS = "RecognizeLetters",
    PT_RECOGNIZE_NUMBERS_AND_LETTERS = "RecognizeNumbersAndLetters",
    PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS = "RecognizeNumbersAndUppercaseLetters",
    PT_RECOGNIZE_UPPERCASE_LETTERS = "RecognizeUppercaseLetters",
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `PT_DEFAULT` | The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "Default". |
| `PT_READ_BARCODES` | The default template for the Barcode Reader that offers a balance between speed and read rate. |
| `PT_READ_BARCODES_SPEED_FIRST` | The speed first template prioritizes speed over read rate when reading barcodes. |
| `PT_READ_BARCODES_READ_RATE_FIRST` | The read rate first template prioritizes read rate over speed when reading barcodes. |
| `PT_READ_SINGLE_BARCODE` | The single barcode template focuses on the single-scan barcode reading mode and should not be used when reading multiple barcodes at a time as it is more speed focused. |
| `PT_RECOGNIZE_TEXT_LINES` | The default template for the Text Line Recognizer. |
| `PT_DETECT_DOCUMENT_BOUNDARIES` | The default template for the Document Boundary Detector. |
| `PT_DETECT_AND_NORMALIZE_DOCUMENT` | The default template for the Document Normalizer. |
| `PT_NORMALIZE_DOCUMENT` | The default template for the Document Normalizer. |
| `PT_RECOGNIZE_NUMBERS` | The default template for the Number Recognizer. |
| `PT_RECOGNIZE_LETTERS` | The default template for the Letter Recognizer. |
| `PT_RECOGNIZE_NUMBERS_AND_LETTERS` | The default template for the Number and Letter Recognizer. |
| `PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS` | The default template for the Number and Uppercase Letter Recognizer. |
| `PT_RECOGNIZE_UPPERCASE_LETTERS` | The default template for the Uppercase Letter Recognizer. |
