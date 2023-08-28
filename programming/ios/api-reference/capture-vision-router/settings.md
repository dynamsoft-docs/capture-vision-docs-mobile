---
layout: default-layout
Title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The APIs of the DSCaptureVisionRouter for processing multiple Images/Pages.
Keywords: capture vision, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Configure Settings

| Method | Description |
| ------ | ----------- |
| [`initSettings`](#initsettings) | Initialize the settings with a JSON String. |
| [`initSettingsFromFile`](#initsettingsfromfile) | Initialize the settings with a JSON file. |
| [`getSimplifiedSettings`](#getsimplifiedsettings) | Retrieves a simplified version of the Capture Vision settings for a specific template. |
| [`updateSettings`](#updatesettings) | Update the Capture Vision settings with an object of `DSSimplifiedCaptureVisionSettings`. |
| [`resetSettings`](#resetsettings) | Reset the Capture Vision settings. |
| [`outputSettings`](#outputsettings) | Output the targeted Capture Vision settings to a JSON string. |
| [`outputSettingsToFile`](#outputsettingstofile) | Output the targeted Capture Vision settings to a JSON file. |

## initSettings

Initialize the settings with a JSON String.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)initSettings:(NSString *)content
               error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func initSettings(_ content:String) throws -> BOOL
```

**Parameters**

`content`: A JSON string that contains Capture Vision settings.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

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

**Return Value**

A BOOL value that indicates whether the settings are initialized successfully.

## initSettingsFromFile

Initialize the settings with a JSON file.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)initSettingsFromFile:(NSString *)file
                        error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func initSettingsFromFile(_ file:String) throws -> BOOL
```

**Parameters**

`file`: A JSON file that contains Capture Vision settings.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

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

**Return Value**

A BOOL value that indicates whether the settings are initialized successfully.

## getSimplifiedSettings

Retrieves a simplified version of the Capture Vision settings for a specific template.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSSimplifiedCaptureVisionSettings *)getSimplifiedSettings:(NSString *)templateName
                                                                error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func getSimplifiedSettings(_ templateName:String) throws -> SimplifiedCaptureVisionSettings
```

**Parameters**

`templateName`: Name of the targeted Capture Vision template that is defined in a JSON string or a JSON file.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CONVERT_COMPLEX_TEMPLATE_ERROR | -10061 | The template you specified is a complex template which can not be output as a `SimplifiedCaptureVisionSettings` object. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Return Value**

A [`DSSimplifiedCaptureVisionSettings`](auxiliary-classes/simplified-capture-vision-settings.md) object.

**Remarks**

A single JSON string or file can define multiple Capture Vision templates. `getSimplifiedSettings` will only return the simplified settings of the template named in the input parameter, even though there could be several templates in the JSON string/file.

## updateSettings

Update the Capture Vision settings with an object of `DSSimplifiedCaptureVisionSettings`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)updateSettings:(NSString *)templateName
              settings:(nonnull DSSimplifiedCaptureVisionSettings *)settings
                 error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func updateSettings(_ templateName:String, settings:SimplifiedCaptureVisionSettings) throws -> BOOL
```

**Parameters**

`templateName`: The name of the template that you want to update.  
`settings`: An object of [`DSSimplifiedCaptureVisionSettings`](auxiliary-classes/simplified-capture-vision-settings.md).  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your `SimplifiedCaptureVisionSettings`. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Return Value**

A bool value that indicates whether the settings are uploaded successfully.

## resetSettings

Reset the Capture Vision settings.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)resetSettings:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func resetSettings() throws -> BOOL
```

**Parameters**

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Return Value**

A BOOL value that indicates whether the settings are reset successfully.

## outputSettings

Output the targeted Capture Vision settings to a JSON string.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable NSString *)outputSettings:(NSString *)templateName
                                error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func outputSettings(_ templateName:String) throws -> String
```

**Parameters**

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Return Value**

The Capture Vision settings in a JSON string.

## outputSettingsToFile

Output the targeted Capture Vision settings to a JSON file.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)outputSettingsToFile:(NSString *)templateName
                        file:(NSString *)file
                       error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func outputSettingsToFile(_ templateName:String, file:String) throws -> BOOL
```

**Parameters**

`templateName`: The name of the template that you want to output.  
`file`: The file path and name where the template will be output and saved.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_SAVE_FAILED | -10058 | The file path is unavailable or the file can't be created for any other reasons. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Return Value**

A BOOL value that indicates whether the template is output successfully.
