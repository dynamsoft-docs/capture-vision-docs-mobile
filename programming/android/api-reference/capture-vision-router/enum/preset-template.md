---
layout: default-layout
title: PresetTemplate - Dynamsoft Vision Router Enumerations
description: The enumeration PresetTemplate of Dynamsoft Vision Router describes the preset template.
keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Enumeration PresetTemplate

`PresetTemplate` describes the preset template names.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumPresetTemplate
{
   /** Template name: "Default". It implements barcode decoding, label recognizing and document normalizing. */
   String PT_DEFAULT = "Default";
   /** Template name: "ReadBarcodes_Default". */
   String PT_READ_BARCODES = "ReadBarcodes_Default";
   /** Template name: "RecognizeTextLines_Default". */
   String PT_RECOGNIZE_TEXT_LINES = "RecognizeTextLines_Default";
   /** Template name: "DetectDocumentBoundaries_Default". */
   String PT_DETECT_DOCUMENT_BOUNDARIES = "DetectDocumentBoundaries_Default";
   /** Template name: "DetectAndNormalizeDocument_Default". */
   String PT_DETECT_AND_NORMALIZE_DOCUMENT = "DetectAndNormalizeDocument_Default";
   /** Template name: "NormalizeDocument_Default". */
   String PT_NORMALIZE_DOCUMENT = "NormalizeDocument_Default";
   /** Template name: "ReadBarcodes_SpeedFirst". */
   String PT_READ_BARCODES_SPEED_FIRST = "ReadBarcodes_SpeedFirst";
   /** Template name: "ReadBarcodes_ReadRateFirst". */
   String PT_READ_BARCODES_READ_RATE_FIRST = "ReadBarcodes_ReadRateFirst";
   /** Template name: "ReadSingleBarcode". */
   String PT_READ_SINGLE_BARCODE = "ReadSingleBarcode";
   /** Template name: "RecognizeNumbers". */
   String PT_RECOGNIZE_NUMBERS = "RecognizeNumbers";
   /** Template name: "RecognizeLetters". */
   String PT_RECOGNIZE_LETTERS = "RecognizeLetters";
   /** Template name: "RecognizeNumbersAndLetters". */
   String PT_RECOGNIZE_NUMBERS_AND_LETTERS = "RecognizeNumbersAndLetters";
   /** Template name: "RecognizeNumbersAndUppercaseLetters". */
   String PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS = "RecognizeNumbersAndUppercaseLetters";
   /** Template name: "RecognizeUppercaseLetters". */
   String PT_RECOGNIZE_UPPERCASE_LETTERS = "RecognizeUppercaseLetters";
}
```
