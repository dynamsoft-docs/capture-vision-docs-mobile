---
layout: default-layout
title: PresetTemplate - Dynamsoft Vision Router iOS Enumerations
description: The enumeration PresetTemplate of Dynamsoft Vision Router iOS describes the preset template.
keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Enumeration PresetTemplate

`PresetTemplate` describes the preset template names.

## Members

### readBarcodes

The default template for the barcode reading tasks.

**Code Snippet**

Specify the preset template in the `startCapturing` method for scanning from the video.

```swift
cvr.startCapturing(PresetTemplate.readBarcodes.rawValue) { isSuccess, error in
    if (!isSuccess) {
        if let error = error {
            self.showResult("Error", error.localizedDescription)
        }
    }
}
```

Specify the preset template in the `capture` method for reading from an image.

```swift
let result = cvr.captureFromFile("Your file path", templateName: PresetTemplate.readBarcodes.rawValue)
```

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

### presetDefault

The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "Default".
