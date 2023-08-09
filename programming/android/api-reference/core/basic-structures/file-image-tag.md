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

## Methods

| Method | Description |
|------- |-------------|
| [`FileImageTag(filePath,pageNumber,totalPages)`](#fileimagetagfilepathpagenumbertotalpages) | The constructor of the FileImageTag. |
| [`getFilePath`](#getfilepath) | Gets the file path of the image. |
| [`getPageNumber`](#getpagenumber) | Gets the page number of the current image in the PDF/Tiff file. |
| [`getTotalPages`](#gettotalpages) | Gets the total page number of the PDF/Tiff file. |

### FileImageTag(filePath,pageNumber,totalPages)

The constructor of the FileImageTag.

```java
FileImageTag(String filePath, int pageNumber, int totalPages);
```

**Parameters**

`[in] imageId`: The ID of the image.  

`[in] filePath`: The file path of the image.

`[in] pageNumber`: The page number of the current image in the PDF file.  

`[in] totalPages`: The total page number of the PDF file.

**Return Value**

An instance of the `FileImageTag`.

### getFilePath

Gets the file path of the image.

```java
String getFilePath();
```

**Return Value**

The file path of the image.

### getPageNumber

Gets the page number of the current image in the PDF/Tiff file.

```java
int getPageNumber();
```

**Return Value**

The page number of the current image in the PDF/Tiff file.

### getTotalPages

Gets the total page number of the PDF/Tiff file.

```java
int getTotalPages();
```

**Return Value**

The total page number of the PDF/Tiff file.