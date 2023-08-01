---
layout: default-layout
Title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The APIs of the CaptureVisionRouter for processing multiple Images/Pages.
Keywords: capture vision, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Configure Settings

| Method | Description |
| ------ | ----------- |
| [`initSettings`](#initsettings) | Initialize the capture settings with a JSON String. |
| [`initSettingsFromFile`](#initsettingsfromfile) | Initialize the capture settings with a JSON file. |
| [`getSimplifiedSettings`](#getsimplifiedsettings) | Retrieves a simplified version of the capture settings for a specific template. |
| [`updateSettings`](#updatesettings) | Update capture vision settings with an object of `SimplifiedCaptureVisionSettings`. |
| [`resetSettings`](#resetsettings) | Resets all templates to factory settings. |
| [`outputSettings`](#outputsettings) | Output the targeting capture vision settings to a JSON string. |
| [`outputSettingsToFile`](#outputsettingstofile) | Output the targeting capture vision settings to a JSON file. |

## initSettings

Initialize the capture settings with a JSON String.

```java
void initSettings(String content) throws CaptureVisionRouterException;
```

**Parameters**

`[in] content`: A JSON string that contains capture vision settings.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

## initSettingsFromFile

Initialize the capture settings with a JSON file.

```java
void initSettingsFromFile(String filePath) throws CaptureVisionRouterException;
```

**Parameters**

`[in] file`: A JSON file that contains capture vision settings.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* There exists invalid parameters in your settings.
* Your file path is unavailable.

## getSimplifiedSettings

Retrieves a simplified version of the capture settings for a specific template.

```java
SimplifiedCaptureVisionSettings getSimplifiedSettings(String templateName) throws CaptureVisionRouterException;
```

**Return Value**

An object of [`SimplifiedCaptureVisionSettings`](./auxiliary-classes/simplified-capture-vision-settings.md).

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You are using a complex template and failed to output the simplified settings object.

## updateSettings

Update capture vision settings with an object of [`SimplifiedCaptureVisionSettings`](./auxiliary-classes/simplified-capture-vision-settings.md).

```java
void updateSettings(String templateName, SimplifiedCaptureVisionSettings settings) throws CaptureVisionRouterException;
```

**Parameters**

`[in] templateName`: Specify the name of the template that you want to update.

`[in] settings`: An object of SimplifiedCaptureVisionSettings.


**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

## resetSettings

Resets all templates to factory settings.

```java
void resetSettings() throws CaptureVisionRouterException;
```

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

## outputSettings

Output the targeting capture vision settings to a JSON string.

```java
String outputSettings(String templateName) throws CaptureVisionRouterException;
```

`[in] templateName`: The name of the template that you want to output.

**Return Value**

The capture vision settings in a JSON string.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* The template name you input is invalid.

## outputSettingsToFile

Output the targeting capture vision settings to a JSON file.

```java
void outputSettingsToFile(String templateName, String filePath) throws CaptureVisionRouterException;
```

**Parameters**

`[in] templateName`: The name of the template that you want to output.

`[in] file`: The file path and name that you want to save the template.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable.
