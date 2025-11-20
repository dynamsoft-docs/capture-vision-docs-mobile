---
layout: default-layout
title: Setting Configuration APIs - Dynamsoft Capture Vision MAUI Edition
description: The APIs of the CaptureVisionRouter MAUI edition for configuring settings - Dynamsoft Capture Vision MAUI Edition
keywords: Init settings, JSON template, Capture Vision Template, reset, simplified settings
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Configure Settings

| Method | Description |
| ------ | ----------- |
| [`InitSettings`](#initsettings) | Configures runtime settings using a provided JSON string, which contains settings for one or more `CaptureVisionTemplates`. |
| [`InitSettingsFromFile`](#initsettingsfromfile) | Configures runtime settings using a provided JSON file, which contains settings for one or more `CaptureVisionTemplates`. |
| [`InitSettingsFromFileAsync`](#initsettingsfromfile) | Configures runtime settings using a provided JSON file, which contains settings for one or more `CaptureVisionTemplates`. This method is asynchronous. |
| [`GetSimplifiedSettings`](#getsimplifiedsettings) | Retrieves a simplified version of the Capture Vision settings for a specific template. |
| [`UpdateSettings`](#updatesettings) | Updates the specified `CaptureVisionTemplate` with an updated `SimplifiedCaptureVisionSettings` object. |
| [`ResetSettings`](#resetsettings) | Restores all settings to their original default values. |
| [`OutputSettings`](#outputsettings) | Returns an object that contains settings for the specified `CaptureVisionTemplate`. |
| [`OutputSettingsToFile`](#outputsettingstofile) | Generates a JSON file download containing the settings for the specified `CaptureVisionTemplate`. |
| [`ClearDLModelBuffers`](#cleardlmodelbuffers) | Clear the buffered deep learning models to release the memory. |
| [`SetGlobalIntraOpNumThreads`](#setglobalintraopnumthreads) | Sets the global number of threads used internally for model execution. |

## InitSettings

Configures runtime settings using a provided JSON string, which contains settings for one or more `CaptureVisionTemplates`.

```csharp
void InitSettings(string content);
```

**Parameters**

`[in] content`: A JSON string that contains Capture Vision settings.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_JSON_PARSE_FAILED | -10030 | Failed to parse the JSON data. |
| EC_JSON_TYPE_INVALID | -10031 | One or more parameters are allocated with wrong data type. |
| EC_JSON_KEY_INVALID | -10032 | There exists invalid key in your JSON data. |
| EC_JSON_VALUE_INVALID | -10033 | There exists invalid parameter value in your JSON data. |
| EC_JSON_NAME_KEY_MISSING | -10034 | One or more `name` parameters are missing in your JSON data. Each section of the JSON data requires a unique `name` parameter. |
| EC_JSON_NAME_VALUE_DUPLICATED | -10035 | There exists duplicated `name` parameters in your JSON data. The `name` parameter should be unique. |
| EC_JSON_NAME_REFERENCE_INVALID | -10037 | You have referenced an invalid `name` value in your JSON data. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## InitSettingsFromFile

Configures runtime settings using a provided JSON file, which contains settings for one or more `CaptureVisionTemplates`.

```csharp
void InitSettingsFromFile(string filePath);
```

**Parameters**

`[in] file`: A JSON file that contains Capture Vision settings.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_JSON_PARSE_FAILED | -10030 | Failed to parse the JSON data. |
| EC_JSON_TYPE_INVALID | -10031 | One or more parameters are allocated with wrong data type. |
| EC_JSON_KEY_INVALID | -10032 | There exists invalid key in your JSON data. |
| EC_JSON_VALUE_INVALID | -10033 | There exists invalid parameter value in your JSON data. |
| EC_JSON_NAME_KEY_MISSING | -10034 | One or more `name` parameters are missing in your JSON data. Each section of the JSON data requires a unique `name` parameter. |
| EC_JSON_NAME_VALUE_DUPLICATED | -10035 | There exists duplicated `name` parameters in your JSON data. The `name` parameter should be unique. |
| EC_JSON_NAME_REFERENCE_INVALID | -10037 | You have referenced an invalid `name` value in your JSON data. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## InitSettingsFromFileAsync

Configures runtime settings using a provided JSON file, which contains settings for one or more `CaptureVisionTemplates`. This method is asynchronous.

```csharp
Task InitSettingsFromFileAsync(string content);
```

**Parameters**

`[in] content`: A real file path or a file name only.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_JSON_PARSE_FAILED | -10030 | Failed to parse the JSON data. |
| EC_JSON_TYPE_INVALID | -10031 | One or more parameters are allocated with wrong data type. |
| EC_JSON_KEY_INVALID | -10032 | There exists invalid key in your JSON data. |
| EC_JSON_VALUE_INVALID | -10033 | There exists invalid parameter value in your JSON data. |
| EC_JSON_NAME_KEY_MISSING | -10034 | One or more `name` parameters are missing in your JSON data. Each section of the JSON data requires a unique `name` parameter. |
| EC_JSON_NAME_VALUE_DUPLICATED | -10035 | There exists duplicated `name` parameters in your JSON data. The `name` parameter should be unique. |
| EC_JSON_NAME_REFERENCE_INVALID | -10037 | You have referenced an invalid `name` value in your JSON data. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your JSON data. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## GetSimplifiedSettings

Retrieves a simplified version of the Capture Vision settings for a specific template.

```csharp
SimplifiedCaptureVisionSettings GetSimplifiedSettings(string templateName);
```

**Parameters**

`templateName`: Specify a template with a templateName for the data capturing.  

**Return Value**

An object of [`SimplifiedCaptureVisionSettings`](./auxiliary-classes/simplified-capture-vision-settings.md).

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CONVERT_COMPLEX_TEMPLATE_ERROR | -10061 | The template you specified is a complex template which can not be output as a `SimplifiedCaptureVisionSettings` object. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## UpdateSettings

Updates the specified `CaptureVisionTemplate` with an updated [`SimplifiedCaptureVisionSettings`](./auxiliary-classes/simplified-capture-vision-settings.md) object.

```csharp
void UpdateSettings(string templateName, SimplifiedCaptureVisionSettings settings);
```

**Parameters**

`[in] templateName`: Specify the name of the template that you want to update.

`[in] settings`: An object of SimplifiedCaptureVisionSettings.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your `SimplifiedCaptureVisionSettings`. |
| EC_CONVERT_COMPLEX_TEMPLATE_ERROR | -10061 | The template you specified is a complex template which can not be updated via a `SimplifiedCaptureVisionSettings` object. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## ResetSettings

Restores all settings to their original default values.

```csharp
void ResetSettings();
```

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## OutputSettings

Returns an object that contains settings for the specified `CaptureVisionTemplate`.

```csharp
string OutputSettings(string templateName);
```

`[in] templateName`: The name of the template that you want to output.

**Return Value**

The Capture Vision settings in a JSON string.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## OutputSettingsToFile

Generates a JSON file download containing the settings for the specified `CaptureVisionTemplate`.

```csharp
void OutputSettingsToFile(string templateName, string filePath);
```

**Parameters**

`[in] templateName`: The name of the template that you want to output.

`[in] file`: The file path and name that you want to save the template.

**Possible Errors**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_SAVE_FAILED | -10058 | The file path is unavailable or the file can't be created for any other reasons. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

## ClearDLModelBuffers

Clear the buffered deep learning models to release the memory.

```csharp
static partial void ClearDLModelBuffers();
```

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.3000 and Dynamsoft Capture Vision version 3.2.3000.

## SetGlobalIntraOpNumThreads

Sets the global number of threads used internally for model execution.

```csharp
static partial void SetGlobalIntraOpNumThreads(int numThreads);
```

**Parameters**

`numThreads`: Number of threads used internally for model execution. Valid range: [0, 256]. Default: 2.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.3000 and Dynamsoft Capture Vision version 3.2.3000.
