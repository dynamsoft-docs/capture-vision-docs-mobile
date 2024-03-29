---
layout: default-layout
title: DirectoryFetcher * Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class DirectoryFetcher of Dynamsoft Capture Vision Router Module is a utility class that retrieves a list of files from a specified directory based on certain criteria.
keywords: directory fetcher, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DirectoryFetcher

> You are viewing a history document page of DynamsoftUtility v1.0.10.

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
| [`DirectoryFetcher`](#directoryfetcher-1) | The constructor. |

### setDirectory

Sets the directory path and filter for the file search.

```java
void setDirectory(String directoryPath, String filter, boolean recursive) throws UtilityException;
```

**Parameters**

`[in] directoryPath`: The directory path.  

`[in] filter`: A string that specifies file extensions. It determines which kinds of files to read. e.g "\*.BMP;\*.JPG;\*.GIF".  

`[in] recursive`: Specifies whether to load files recursively.  

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_READ_DIRECTORY_FAILED | -10064 | Failed to read the directory. |

<!-- 
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
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. | -->

### DirectoryFetcher

The constructor.

```java
DirectoryFetcher()
```
