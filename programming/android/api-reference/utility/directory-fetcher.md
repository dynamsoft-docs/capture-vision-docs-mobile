---
layout: default-layout
Title: DSDirectoryFetcher * Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class DSDirectoryFetcher of Dynamsoft Capture Vision Router Module is a utility class that retrieves a list of files from a specified directory based on certain criteria.
Keywords: directory fetcher, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSDirectoryFetcher

The `DSDirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `DSImageSourceAdapter` class.

## Definition

*Namespace*: com.dynamsoft.utility  
*Assembly:* DynamsoftUtility.aar

```java
class DirectoryFetcher extends ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`init`](#init) | Create an instance of DSDirectoryFetcher. |
| [`setDirectory`](#setdirectory) | Sets the directory path and filter for the file search. |
| [`setPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters for reading PDF files. |

### init

Create an instance of DSDirectoryFetcher.

```java
init()
```

**Return Value**

An instance of `DSDirectoryFetcher`.

### setDirectory

Sets the directory path and filter for the file search.

```java
func setDirectory(_ directoryPath: String, filter: String?, recursive: Bool) throws
```

**Parameters**

`directoryPath`: The directory path.  
`filter`: A string that specifies file extensions. It determines which kinds of files to read. e.g ".BMP;.JPG;.GIF".  
`recursive`: Specifies whether to load files recursively.  
`error`: A `NSError` pointer. An error occurs when:

* The directory is unavailable.
* The method is triggered after the capture is started.

**Return Value**

A `BOOL` value that indicates whether the directory is set successfully.

### setPDFReadingParameter

Sets the parameters for reading PDF files.

```java
func setPDFReadingParameter(_ para: DSPDFReadingParameter) throws
```

**Parameters**

`para`: A `DSPDFReadingParameter` object.
`error`: A `NSError` pointer. An error occurs when:

* The directory is unavailable.
* The method is triggered after the capture is started.

**Return Value**

A `BOOL` value that indicates whether the PDF reading mode is set successfully.
