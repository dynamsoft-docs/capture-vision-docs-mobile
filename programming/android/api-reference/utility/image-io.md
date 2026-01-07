---
layout: default-layout
title: ImageIO - Dynamsoft Capture Vision Android Edition API Reference
description: The class ImageIO of Dynamsoft Capture Vision Android is a utility class for managing the image data. It provides functionality for saving images to files and reading images from files.
keywords: image io, image manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageIO

The class `ImageIO` is a utility class for managing the image data. It provides functionality for saving images to files and reading images from files.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class ImageIO
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`readFromFile`](#readfromfile) | Reads an image from the specified path and format. |
| [`readFromMemory`](#readfrommemory) | Reads an image from the memory. |
| [`saveToFile`](#savetofile) | Saves an image to the specified path and format. |
| [`saveToMemory`](#savetomemory) | Saves an image to the memory. |

### saveToFile

Saves an image to the specified path and format. The desired file format is inferred from the file extension provided in the `path` parameter.

```java
void saveToFile(@NonNull ImageData imageData, @NonNull String path, boolean overWrite) throws UtilityException{}
```

**Parameters**

`[in] imageData`: The image to be saved, of type `ImageData`.

`[in] path`: The file path, name and extension name, as a string, under which the image will be saved.

`[in] overWrite`: A flag indicating whether to overwrite the file if it already exists. Defaults to true.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**Return Value**

A boolean value that indicates whether the file is saved successfully.

**Code Snippet**

```java
@Override
public void onOriginalImageResultReceived(@NonNull OriginalImageResultItem result) {
    if (result != null)
    {
        ImageIO imageManager = new ImageIO();
        Thread saveThread = new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    imageManager.saveToFile(result.getImageData(), String.valueOf(Environment.getExternalStoragePublicDirectory(Environment.DIRECTORY_PICTURES))+"/DynamsoftImageIO/originalImage.png", true);
                } catch (UtilityException e) {
                    throw new RuntimeException(e);
                } catch (CoreException e) {
                    throw new RuntimeException(e);
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
        });
        saveThread.start();
    } else {
        Log.i("CRR", "onOriginalImageResultReceived: Not saved");
        return;
    }
}
```

### saveToMemory

Saves an image to the memory.

```java
byte[] SaveToMemory(@NonNull ImageData imageData, @EnumImageFileFormat int imageFormat) throws UtilityException{}
```

**Parameters**

`[in] imageData`: The image to be saved, of type `ImageData`.

`[in] imageFormat`: The image format.

**Return Value**

The image bytes.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

### readFromFile

Reads an image from the specified path and format.

```java
ImageData readFromFile(@NonNull String filePath) throws UtilityException{}
```

**Parameters**

`[in] filePath`: The file path, name and extension name, as a string, from which the image will be read.

**Return Value**

The image data of type `ImageData`.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |

### readFromMemory

Reads an image from the memory.

```java
ImageData readFromMemory(@NonNull byte[] fileBytes) throws UtilityException{}
```

**Parameters**

`[in] fileBytes`: The image bytes.

**Return Value**

The image data of type `ImageData`.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |
