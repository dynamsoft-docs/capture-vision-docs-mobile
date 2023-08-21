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
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture starts or after `startCapturing` is invoked.
* The settings string includes invalid parameters.

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
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture starts or after `startCapturing` is invoked.
* The settings template contains some invalid parameters.
* The file path is unavailable or unaccessable.

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
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture starts or after `startCapturing` is invoked.
* You are using a very complex template and the library fails to output the simplified settings object.
* The Capture Vision template that is referenced doesn't exist in the overall template file or string.

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
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture starts or after `startCapturing` is invoked.
* The settings object contains some invalid parameters.

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

`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture starts or after `startCapturing` is invoked.
* The settings object contains some invalid parameters.

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

`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture starts or after `startCapturing` is invoked.
* The template name is invalid or doesn't exist in the JSON string/file.

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
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture starts or after `startCapturing` is invoked.
* The template name is invalid or doesn't exist.
* The file path you input is unavailable or inaccessible.

**Return Value**

A BOOL value that indicates whether the template is output successfully.
