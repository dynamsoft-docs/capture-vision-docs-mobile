---
layout: default-layout
Title: DSFileFetcher * Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class DSFileFetcher of Dynamsoft Capture Vision Router Module is a utility class that partitions a multi-page image file into multiple independent ImageData objects.
Keywords: file fetcher, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSFileFetcher

The `DSFileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `DSImageSourceAdapter` class.

## Definition

*Namespace*: com.dynamsoft.utility  
*Assembly:* DynamsoftUtility.aar

```java
class FileFetcher
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`filePath`](#filepath) | *NSString \** | The file path. |
| [`fileBytes`](#filebytes) | *NSData \** | The file bytes. |
| [`buffer`](#buffer) | *DSImageData \** | The image data. |
| [`image`](#image) | *UIImage \** | A `UIImage`. |
| [`para`](#para) | *PDFReadingParameter \** | The parameter object for reading PDF files. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`setFileWithPath`](#setfilewithpath) | Sets the file with a file path. |
| [`setFileWithBytes`](#setfilewithbytes) | Sets the file with file bytes. |
| [`setFileWithBuffer`](#setfilewithbuffer) | Sets the file with a `DSImageData` object. |
| [`setFileWithImage`](#setfilewithimage) | Sets the file with a `UIImage`. |
| [`setPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters of PDF reading. |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Whether there is a next image to fetch. |
| [`getImage`](#getimage) | Get the image data of the image. |

### filePath

The file path.

```java
var filePath: String? { get set }
```

### fileBytes

The file bytes.

```java
var fileBytes: Data? { get set }
```

### buffer

The image data.

```java
var buffer: ImageData? { get set }
```

### image

A `UIImage`.

```java
var image: UIImage? { get set }
```

### para

The parameter object for reading PDF files.

```java
var para: PDFReadingParameter? { get set }
```

### setFileWithPath

Sets the file with a file path.

```java
func setFile(withPath filePath: String) throws
```

**Parameters**

`filePath`: The file path.

`error`: An `NSError` pointer. An error occurs when fail to load the image.

### setFileWithBytes

Sets the file with file bytes.

```java
func setFile(withBytes fileBytes: Data) throws
```

**Parameters**

`fileBytes`: The file bytes.  
`error`: An `NSError` pointer. An error occurs when fail to load the image.

### setFileWithBuffer

Sets the file with a `DSImageData` object.

```java
func setFile(withBuffer buffer: ImageData) throws
```

**Parameters**

`buffer`: The image data.

`error`: An `NSError` pointer. An error occurs when fail to load the image.

### setFileWithImage

Sets the file with a `UIImage`.

```java
func setFile(withImage image: UIImage) throws
```

**Parameters**

`image`: A `UIImage`.

`error`: An `NSError` pointer. An error occurs when fail to load the image.

### setPDFReadingParameter

Sets the parameters of PDF reading.

```java
func setPDFReadingParameter(_ para: PDFReadingParameter) throws
```

**Parameters**

`para`: The parameter object for reading PDF files.

`error`: An `NSError` pointer. An error occurs when:

* The directory is unavailable.
* The method is triggered after the capture is started.

**Return Value**

A BOOL value that indicates whether the PDF reading mode is set successfully.

### hasNextImageToFetch

Whether there is a next image to fetch.

```java
func hasNextImageToFetch() -> Bool
```

**Return Value**

A bool value that indicates whether there is a next image to fetch.

### getImage

Get the image data of the image.

```java
func getImage() -> ImageData
```

**Return Value**

A `DSImageData` as the image.
