---
layout: default-layout
Title: Processing a Single Image - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The APIs of the CaptureVisionRouter for processing a single image.
Keywords: capture vision, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing a Single Image

| Method | Description |
| ------ | ----------- |
| [`captureFromFile`](#capturefromfile) | Implement data capture on the given file. |
| [`captureFromFileBytes`](#capturefromfilebytes) | Implement data capture on the given file in memory. |
| [`captureFromBuffer`](#capturefrombuffer) | Implement data capture on the given image data. |
| [`captureFromImage`](#capturefromimage) | Implement data capture on the given UIImage. |

## captureFromFile

Implement data capture on the given file.

```java
func captureFromFile(_ file:String, templateName:String) throws -> CaptureResult
```

**Parameters**

`file`: The file path and name that you want to implement the data capturing.
`templateName`: Specify a template with a templateName for the data capturing.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNG files).

**Return Value**

A CapturedResult object output by the library.

## captureFromFileBytes

Implement data capture on the given file in memory.

```java
func captureFromFileBytes(_ fileBytes:Data, templateName:String) throws -> CaptureResult
```

**Parameters**

`fileBytes`: A NSData that points to a file in memory.
`templateName`: Specify a template with a templateName for the data capturing.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNGles).

**Return Value**

A `CapturedResult` object output by the library.

## captureFromBuffer

Implement data capture on the given file.

```java
func captureFromBuffer(_ buffer:DSImageData, templateName:String) throws -> CaptureResult
```

**Parameters**

`buffer`: A DSImageData object that contains image info.
`templateName`: Specify a template with a templateName for the data capturing.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The image buffer is invalid.

**Return Value**

A CapturedResult object output by the library.

## captureFromImage

Implement data capture on the given file.

```java
func captureFromBuffer(_ image:UIImage, templateName:String) throws -> CaptureResult
```

**Parameters**

`image`: A UIImage.
`templateName`: Specify a template with a templateName for the data capturing.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.

**Return Value**

A `CapturedResult` object output by the library.
