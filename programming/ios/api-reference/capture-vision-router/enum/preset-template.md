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

## Definition

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NSString * DSPresetTemplate NS_STRING_ENUM NS_SWIFT_NAME(PresetTemplate);
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDefault NS_SWIFT_NAME(presetDefault);
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateReadBarcodes NS_SWIFT_NAME(readBarcodes);
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateRecognizeTextLines NS_SWIFT_NAME(recognizeTextLines);
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDetectDocumentBoundaries NS_SWIFT_NAME(detectDocumentBoundaries);
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDetectAndNormalizeDocument NS_SWIFT_NAME(detectAndNormalizeDocument);
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateNormalizeDocument NS_SWIFT_NAME(normalizeDocument);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateReadBarcodesSpeedFirst NS_SWIFT_NAME(readBarcodesSpeedFirst);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateReadBarcodesReadRateFirst NS_SWIFT_NAME(readBarcodesReadRateFirst);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateReadSingleBarcode NS_SWIFT_NAME(readSingleBarcode);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeNumbers NS_SWIFT_NAME(recognizeNumbers);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeLetters NS_SWIFT_NAME(recognizeLetters);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeNumbersAndLetters NS_SWIFT_NAME(recognizeNumbersAndLetters);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeNumbersAndUppercaseLetters NS_SWIFT_NAME(recognizeNumbersAndUppercaseLetters);
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeUppercaseLetters NS_SWIFT_NAME(recognizeUppercaseLetters);
```
>
```swift
struct PresetTemplate
{
   static let default = "default"
   static let readBarcodes = "read-barcodes"
   static let recognizeTextLines = "recognize-textLines"
   static let detectDocumentBoundaries = "detect-document-boundaries"
   static let detectAndNormalizeDocument = "DetectAndNormalizeDocument_Default"
   static let normalizeDocument = "NormalizeDocument_Default"
   static let readBarcodesSpeedFirst = "ReadBarcodes_SpeedFirst"
   static let readBarcodesReadRateFirst = "ReadBarcodes_ReadRateFirst"
   static let readSingleBarcode = "ReadSingleBarcode"
   static let recognizeNumbers = "RecognizeNumbers"
   static let recognizeLetters = "RecognizeLetters"
   static let recognizeNumbersAndLetters = "RecognizeNumbersAndLetters"
   static let recognizeNumbersAndUppercaseLetters = "RecognizeNumbersAndUppercaseLetters"
   static let recognizeUppercaseLetters = "RecognizeUppercaseLetters"
}
```

## Members

### presetDefault

The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "Default".

### readBarcodes

The default template for the barcode reading tasks.

### readBarcodesSpeedFirst

The barcode reading template that prioritizes speed over read rate.

### readBarcodesReadRateFirst

The barcode reading template that prioritizes read rate over speed.

### readSingleBarcode

The barcode reading template that specifically focuses on the single-barcode-scanning scenario.

### recognizeTextLines

The preset template for the text line recognition tasks.

### recognizeNumbers

The preset template for the number recognition tasks.

### recognizeLetters

The preset template for the letter recognition tasks.

### recognizeNumbersAndLetters

The preset template for the number and letter recognition tasks.

### recognizeNumbersAndUppercaseLetters

The preset template for the number and uppercase letter recognition tasks.

### recognizeUppercaseLetters

The preset template for the uppercase letter recognition tasks.

### detectDocumentBoundaries

The default template for the document boundary detection.

### detectAndNormalizeDocument

The default template for the document detection and normalization.

### normalizeDocument

The default template for the document normalization.
