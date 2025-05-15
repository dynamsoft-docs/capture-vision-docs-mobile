---
layout: default-layout
title: Add Resource Files - Dynamsoft Capture Vision Android Edition
description: This page introduce how to add additional resource files for Dynamsoft Capture Vision Android Edition.
keywords: Android, resource files
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Setup Resources

This page is the guide of how to setup resources for Dynamsoft Capture Vision Android Edition.

1. Right click on your project folder, select **New**, then select **Directory** and select the **src\main\assets** to create an assets folder.

2. Under the **assets** folder create a new folder and name it based on the type of your resource file.

   For example, if you want to setup a template file `ReadVIN.json`, you have to create a new folder named **Templates**. If you want to setup a model file `VINCharRecognition.data` and a template file `ReadVIN.json` at the same time, you have to create two new folders, **Models** and **Templates**.

   | Folder Name | Description |
   | ----------- | ----------- |
   | `Templates` | JSON files that define how to read barcode, scan mrz, etc. |
   | `Models` | Mainly are deep learning models that improves the barcode or text line read rate. |
   | `ConfusableChars` | Resource files for text line recognition. Help distinguish easily confused characters. "0", "O". It helps improving the character recognition accuracy. |
   | `Dictionary` | The resource files used to assist in result validation. The recognition result can be corrected if it matches a word in the dictionary. |
   | `OverlappingChars` | The resource files used to validate or correct recognition results by overlaying standard characters with the recognized characters. |
   | `ParserResources` | The resource files that defines the content parsing rules. |

3. Copy your resource files to the folder you just created.

4. For the template files, here is an additional step. You have to use `initSettingsFromFile` to load your template file. Template file name should be specified as the `filePath` in the `initSettingsFromFile` method. For the other resource files, you don't need this step.

   ```java
   try {
       mRouter.initSettingsFromFile("ReadVIN.json");
   } catch (CaptureVisionRouterException e) {
       throw new RuntimeException(e);
   }
   ```
