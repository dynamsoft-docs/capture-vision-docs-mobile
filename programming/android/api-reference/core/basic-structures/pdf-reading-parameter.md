---
layout: default-layout
Title: PDFReadingParameter - Dynamsoft Core Module Android Edition API Reference
Description: The class PDFReadingParameter of Dynamsoft Core Module represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the target type.
Keywords: PDF reading parameter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PDFReadingParameter

The `PDFReadingParameter` class represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the target type.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

```java
class PDFReadingParameter
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`mode`](#mode) | *int* | Set the processing mode of the PDF file. You can either read the PDF info from vecter data or transform the PDF file into an image. The library will transform the PDF file into an image by default. |
| [`dpi`](#dpi) | *int* | Set the DPI (dots per inch) of the PDF file. |
| [`type`](#type) | *int* | Set the target type of the image. The default type is page. |

### mode

Set the processing mode of the PDF file. You can either read the PDF info from vector data or transform the PDF file into an image. The library will transform the PDF file into an image by default.

```java
int mode;
```

### dpi

Set the DPI (dots per inch) of the PDF file.

```java
int dpi;
```

### type

Set the target type of the image. The default type is page.

```java
int type;
```
