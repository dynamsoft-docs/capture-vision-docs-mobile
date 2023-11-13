---
layout: default-layout
title: DirectoryFetcher - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class DirectoryFetcher of Dynamsoft Capture Vision Router Module is a utility class that retrieves a list of files from a specified directory based on certain criteria.
keywords: directory fetcher, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DirectoryFetcher

The `DirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `ImageSourceAdapter` class.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftUtility.aar

```java
class DirectoryFetcher extends ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`setDirectory`](#setdirectory) | Sets the directory path and filter for the file search. |
| [`setPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters for reading PDF files. |
| [`setPages`](#setpages) | Set the pages to read. |
| [`DirectoryFetcher`](#directoryfetcher-1) | The constructor. |

### setDirectory

Sets the directory path and filter for the file search.

```java
void setDirectory(String directoryPath, String filter, boolean recursive) throws UtilityException;
```

**Parameters**

`[in] directoryPath`: The directory path.  

`[in] filter`: A string that specifies file extensions. It determines which kinds of files to read. e.g ".BMP;.JPG;.GIF".  

`[in] recursive`: Specifies whether to load files recursively.  

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_READ_DIRECTORY_FAILED | -10064 | Failed to read the directory. |

### setPDFReadingParameter

Sets the parameters for reading PDF files.

```java
void setPDFReadingParameter(PDFReadingParameter para) throws UtilityException;
```

**Parameters**

`[in] para`: A `PDFReadingParameter` object.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |

### setPages

Set the pages to read.

```java
void setPages(int[] pages) throws UtilityException;
```

**Parameters**

`pages`: An array that contains all the pages to read.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND  | -10005 | File not found. |
| EC_FILE_TYPE_NOT_SUPPORTED  | -10006 | The file type is not supported. |
| EC_IMAGE_READ_FAILED  | -10012 | Failed to read the image. |
| EC_PDF_READ_FAILED  | -10021 | Failed to read the PDF image. |

### DirectoryFetcher

The constructor.

```java
DirectoryFetcher()
```
