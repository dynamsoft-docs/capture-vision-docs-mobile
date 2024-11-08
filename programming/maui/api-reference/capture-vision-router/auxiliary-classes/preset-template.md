---
layout: default-layout
title: EnumPresetTemplate - Dynamsoft Vision Router MAUI Edition
description: The enumeration PresetTemplate of Dynamsoft Vision Router describes the preset template.
keywords: CaptureVisionTemplate, PresetTemplate, single barcode template, speed first, read-rate first
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: PresetTemplate
---

# EnumPresetTemplate

`EnumPresetTemplate` class defines the preset tempate strings. These strings can be used when specifying template name with [`StartCapturing`](../multiple-file-processing.md#startcapturing) or [`Capture`](../single-file-processing.md#capture) methods.

## Definition

*Namespace:* Dynamsoft.CaptureVisionRouter.Maui

*Assembly:* Dynamsoft.CaptureVisionRouter.Maui

```csharp
public class EnumPresetTemplate
{
    public const string PT_DEFAULT = "Default";
    public const string PT_READ_BARCODES = "ReadBarcodes_Default";
    public const string PT_READ_BARCODES_SPEED_FIRST = "ReadBarcodes_SpeedFirst";
    public const string PT_READ_BARCODES_READ_RATE_FIRST = "ReadBarcodes_ReadRateFirst";
    public const string PT_READ_SINGLE_BARCODE = "ReadSingleBarcode";

    public const string PT_RECOGNIZE_TEXT_LINES = "RecognizeTextLines_Default";
    public const string PT_RECOGNIZE_NUMBERS = "RecognizeNumbers";
    public const string PT_RECOGNIZE_LETTERS = "RecognizeLetters";
    public const string PT_RECOGNIZE_NUMBERS_AND_LETTERS = "RecognizeNumbersAndLetters";
    public const string PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS = "RecognizeNumbersAndUppercaseLetters";
    public const string PT_RECOGNIZE_UPPERCASE_LETTERS = "RecognizeUppercaseLetters";

    public const string PT_DETECT_DOCUMENT_BOUNDARIES = "DetectDocumentBoundaries_Default";
    public const string PT_DETECT_AND_NORMALIZE_DOCUMENT = "DetectAndNormalizeDocument_Default";
    public const string PT_NORMALIZE_DOCUMENT = "NormalizeDocument_Default";
}
```
