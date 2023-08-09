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
| [`getSimplifiedSettings`](#getsimplifiedsettings) | Retrieves a simplified version of the capture settings for a specific template. |
| [`updateSettings`](#updatesettings) | Update capture vision settings with a object of `DSSimplifiedCaptureVisionSettings`. |
| [`resetSettings`](#resetsettings) | Reset the capture vision settings. |
| [`outputSettings`](#outputsettings) | Output the targeting capture vision settings to a JSON string. |
| [`outputSettingsToFile`](#outputsettingstofile) | Output the targeting capture vision settings to a JSON file. |

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

`content`: A JSON string that contains capture vision settings.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

**Return Value**

A bool value that indicates whether the settings are initialized successfully.

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

`file`: A JSON file that contains capture vision settings.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* There exists invalid parameters in your settings.
* Your file path is unavailable.

**Return Value**

A bool value that indicates whether the settings are initialized successfully.

## getSimplifiedSettings

Retrieves a simplified version of the capture settings for a specific template.

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

`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* You are using a complex template and failed to output the simplified settings object.

**Return Value**

An object of `DSSimplifiedCaptureVisionSettings`.

## updateSettings

Update capture vision settings with a object of `DSSimplifiedCaptureVisionSettings`.

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

`templateName`: Specify the name of the template that you want to update.
`settings`: An object of DSSimplifiedCaptureVisionSettings.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* You settings include invalid parameters.

**Return Value**

A bool value that indicates whether the settings are uploaded successfully.

## resetSettings

Reset the capture vision settings.

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

* The method is triggered after the capture is started.
* You settings include invalid parameters.

**Return Value**

A bool value that indicates whether the settings are reset successfully.

## outputSettings

Output the targeting capture vision settings to a JSON string.

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

* The method is triggered after the capture is started.
* The template name you input is invalid.

**Return Value**

The capture vision settings in a JSON string.

## outputSettingsToFile

Output the targeting capture vision settings to a JSON file.

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
`file`: The file path and name that you want to save the template.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable.

**Return Value**

A BOOL value that indicates whether the template is output successfully.