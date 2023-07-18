---
layout: default-layout
Title: DSPDFReadingParameter - Dynamsoft Core Module Android Edition API Reference
Description: The class DSPDFReadingParameter of Dynamsoft Core Module represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the target type.
Keywords: PDF reading parameter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSPDFReadingParameter

The `DSPDFReadingParameter` class represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the target type.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class PDFReadingParameter
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`mode`](#mode) | *DSPDFReadingMode* | Set the processing mode of the PDF file. You can either read the PDF info from vecter data or transform the PDF file into an image. The library will transform the PDF file into an image by default. |
| [`dpi`](#dpi) | *NSInteger* | Set the DPI (dots per inch) of the PDF file. |
| [`type`](#type) | *DSTargetType* | Set the target type of the image. The default type is page. |

### mode

Set the processing mode of the PDF file. You can either read the PDF info from vector data or transform the PDF file into an image. The library will transform the PDF file into an image by default.

```java
var mode: PDFReadingMode { get set }
```

### dpi

Set the DPI (dots per inch) of the PDF file.

```java
var dpi: Int { get set }
```

### type

Set the target type of the image. The default type is page.

```java
var type: TargetType { get set }
```
