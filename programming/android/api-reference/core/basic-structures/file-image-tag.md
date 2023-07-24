---
layout: default-layout
Title: FileImageTag - Dynamsoft Core Module Android Edition API Reference
Description: The class FileImageTag of Dynamsoft Core Module represents an image tag that is associated with a file, which contains the file path, page number, and total page number.
Keywords: image tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# FileImageTag

The `FileImageTag` class represents an image tag that is associated with a file. It inherits from the `ImageTag` class and adds additional attributes.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

```java
class FileImageTag extends ImageTag
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`getFilePath`](#getfilepath) | *String* | The file path of the image. |
| [`getPageNumber`](#getpagenumber) | *int* | The page number of the current image in the PDF file. |
| [`getTotalPages`](#gettotalpages) | *int* | The total page number of the PDF file. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`FileImageTag(filePath,pageNumber,totalPages)`](#fileimagetagfilepathpagenumbertotalpages) | The constructor of the FileImageTag. |

### getFilePath

The file path of the image.

```java
String getFilePath();
```

### getPageNumber

The page number of the current image in the PDF file.

```java
int getPageNumber();
```

### getTotalPages

The total page number of the PDF file.

```java
int getTotalPages();
```

### FileImageTag(filePath,pageNumber,totalPages)

The constructor of the FileImageTag.

```java
FileImageTag(String filePath, int pageNumber, int totalPages);
```

**Parameters**

`imageId`: The ID of the image.  
`filePath`: The file path of the image.  
`pageNumber`: The page number of the current image in the PDF file.  
`totalPages`: The total page number of the PDF file.

**Return Value**

An instance of the `FileImageTag`.
