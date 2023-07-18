---
layout: default-layout
Title: DSFileImageTag - Dynamsoft Core Module Android Edition API Reference
Description: The class DSFileImageTag of Dynamsoft Core Module represents an image tag that is associated with a file, which contains the file path, page number, and total page number.
Keywords: image tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSFileImageTag

The `DSFileImageTag` class represents an image tag that is associated with a file. It inherits from the `DSImageTag` class and adds additional attributes.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class FileImageTag extends ImageTag
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`filePath`](#filepath) | *NSString \** | The file path of the image. |
| [`pageNumber`](#pagenumber) | *NSInteger* | The page number of the current image in the PDF file. |
| [`totalPages`](#totalpages) | *NSInteger* | The total page number of the PDF file. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`initWithImageId`](#initwithimageid) | The constructor of the FileImageTag. |

### filePath

The file path of the image.

```java
var filePath: String? { get }
```

### pageNumber

The page number of the current image in the PDF file.

```java
var pageNumber: Int { get }
```

### totalPages

The total page number of the PDF file.

```java
var totalPages: Int { get }
```

### initWithImageId

The constructor of the FileImageTag.

```java
init(imageId: Int, filePath: String, pageNumber: Int, totalPages: Int)
```

**Parameters**

`imageId`: The ID of the image.  
`filePath`: The file path of the image.  
`pageNumber`: The page number of the current image in the PDF file.  
`totalPages`: The total page number of the PDF file.

**Return Value**

An instance of the `DSFileImageTag`.
