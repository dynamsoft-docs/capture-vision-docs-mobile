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
| [`initSettings`](#initsettings) | Initialize the settings with a JSON String. |
| [`initSettingsFromFile`](#initsettingsfromfile) | Initialize the settings with a JSON file. |
| [`getSimplifiedSettings`](#getsimplifiedsettings) | Get the object of the currently active `SimplifiedCaptureVisionSettings`. |
| [`updateSettings`](#updatesettings) | Update capture vision settings with a object of `SimplifiedCaptureVisionSettings`. |
| [`resetSettings`](#resetsettings) | Reset the capture vision settings. |
| [`outputSettings`](#outputsettings) | Output the targeting capture vision settings to a JSON string. |
| [`outputSettingsToFile`](#outputsettingstofile) | Output the targeting capture vision settings to a JSON file. |

## initSettings

Initialize the settings with a JSON String.

```java
void initSettings(String content) throws CaptureVisionRouterException;
```

**Parameters**

`content`: A JSON string that contains capture vision settings.

**Return Value**

A boolean value that indicates whether the settings are initialized successfully.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

## initSettingsFromFile

Initialize the settings with a JSON file.

```java
void initSettingsFromFile(String filePath) throws CaptureVisionRouterException;
```

**Parameters**

`file`: A JSON file that contains capture vision settings.

**Return Value**

A boolean value that indicates whether the settings are initialized successfully.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* There exists invalid parameters in your settings.
* Your file path is unavailable.

## getSimplifiedSettings

Get the object of the currently active `SimplifiedCaptureVisionSettings`.

```java
SimplifiedCaptureVisionSettings getSimplifiedSettings(String templateName) throws CaptureVisionRouterException;
```

**Return Value**

An object of `SimplifiedCaptureVisionSettings`.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You are using a complex template and failed to output the simplified settings object.

## updateSettings

Update capture vision settings with a object of `SimplifiedCaptureVisionSettings`.

```java
void updateSettings(String templateName, SimplifiedCaptureVisionSettings settings) throws CaptureVisionRouterException;
```

**Parameters**

`templateName`: Specify the name of the template that you want to update.
`settings`: An object of SimplifiedCaptureVisionSettings.

**Return Value**

A boolean value that indicates whether the settings are uploaded successfully.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

## resetSettings

Reset the capture vision settings.

```java
void resetSettings() throws CaptureVisionRouterException;
```

**Return Value**

A boolean value that indicates whether the settings are reset successfully.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

## outputSettings

Output the targeting capture vision settings to a JSON string.

```java
String outputSettings(String templateName) throws CaptureVisionRouterException;
```

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

`templateName`: The name of the template that you want to output.
`file`: The file path and name that you want to save the template.

**Return Value**

A boolean value that indicates whether the template is output successfully.

**Exception**

An exception is thrown when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable.
