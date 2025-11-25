---
layout: default-layout
title: CaptureVisionRouter - Dynamsoft Capture Vision Flutter
description: CaptureVisionRouter class of Dynamsoft Capture Vision Router contains all of the core methods to use Dynamsoft Capture Vision.
keywords: CaptureVisionRouter, Barcode Reader, capture, flutter, foundational
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CaptureVisionRouter
---

# CaptureVisionRouter Class

The `CaptureVisionRouter` class defines how a user interacts with image-processing and semantic-processing Dynamsoft products in their applications.

A `CaptureVisionRouter` instance accepts and processes images from an image source and returns processing results which may contain final results or intermediate results. The instance can also process video frames coming from a camera or a different image source as well, therefore providing the ability to capture results via an interactive video scenario or from static images.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class CaptureVisionRouter
```

## Static Properties

Returns the singleton instance of `CaptureVisionRouter`.

```dart
static CaptureVisionRouter get instance;
```

## Methods

Capture from an Image

| Method | Description |
| ------ | ----------- |
| [`capture`](#capture) | Processes an image using the specified template and outputs a CapturedResult. |
| [`captureFile`](#capturefile) | Processes an image from a file path using the specified template. |
| [`captureFileBytes`](#capturefilebytes) | Processes an image from a byte array using the specified template. |

Process Multiple Images

| Method | Description |
| ------ | ----------- |
| [`addResultFilter`](#addresultfilter) | Adds a result filter to process the captured results. |
| [`addResultReceiver`](#addresultreceiver) | Adds a result receiver that listens for any captured results. |
| [`removeAllResultFilters`](#removeallresultfilters) | Removes all the result filters from the Capture Vision Router instance. |
| [`removeAllResultReceivers`](#removeallresultreceivers) | Removes all result receivers from the Capture Vision Router instance. |
| [`removeResultFilter`](#removeresultfilter) | Removes a previously added result filter. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes a previously added result receiver. |
| [`setInput`](#setinput) | Sets up an image source to provide images for continuous processing. |
| [`startCapturing`](#startcapturing) | Starts the capturing process using the specified template. |
| [`stopCapturing`](#stopcapturing) | Stops the capturing process and closes the camera. |
| [`switchCapturingTemplate`](#switchcapturingtemplate) | Switches the template used by the Capture Vision Router instance to the specified template name. |

Settings

| Method | Description |
| ------ | ----------- |
| [`clearDLModelBuffers`](#cleardlmodelbuffers) | Clears the buffer used by deep learning models to free up memory. |
| [`getSimplifiedSettings`](#getsimplifiedsettings) | Returns a simplified version of the Capture Vision settings for a specific template. |
| [`getTemplateNames`](#gettemplatenames) | Returns a list of all currently available Capture Vision template names. |
| [`initSettings`](#initsettings) | Initializes the settings using a JSON template string. |
| [`initSettingsFromFile`](#initsettingsfromfile) | Initializes the settings using a JSON template file. |
| [`outputSettings`](#outputsettings) | Outputs the specified template's settings as a JSON string. |
| [`outputSettingsToFile`](#outputsettingstofile) | Outputs the specified template's settings to a JSON file. |
| [`resetSettings`](#resetsettings) | Resets all settings to their default values. |
| [`updateSettings`](#updatesettings) | Updates the specified template settings using a `SimplifiedCaptureVisionSettings` object. |
| [`setGlobalIntraOpNumThreads`](#setglobalintraopnumthreads) | Sets the global number of threads used internally by the library for model execution. |

Intermediate Results

| Method | Description |
| ------ | ----------- |
| [`getIntermediateResultManager`](#getintermediateresultmanager) | Retrieves the IntermediateResultManager instance. |

### capture

Processes an image using the specified template.

```dart
Future<CapturedResult> capture(ImageData imageData, String templateName) async
```

**Parameters**

`[in] imageData`: A [`ImageData`]({{ site.dcv_flutter_api }}core/image-data.html) object that contains image info.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

### captureFile

Processes an image from a file (specified by a file path) using the specified template.

```dart
Future<CapturedResult> captureFile(String filePath, String templateName) async
```

**Parameters**

`[in] filePath`: The file path and name that you want to capture data from. You have to specify the file name with extension name in the `filePath`. Supported file type includes ".bmp", ".jpg", ".png", ".gif" or one-page ".tiff".

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

### captureFileBytes

Processes an image from a byte array using the specified template.

```dart
Future<CapturedResult> captureFileBytes(Uint8List bytes, String templateName) async
```

**Parameters**

`[in] bytes`: A byte array that points to a file in memory.

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

### addResultFilter

Adds a result filter to process the captured results. This filter is of type [`MultiFrameResultCrossFilter`](multi-frame-cross-filter.md). Supported filters:

- Cross-Verification: Improve the accuracy by cross-verifying the results.
- De-duplication: Removes the duplicated results.
- Overlapping: Improve the read-rate of multiple barcode scanning by overlaping the results.

```dart
Future<void> addResultFilter(MultiFrameResultCrossFilter filter)
```

### addResultReceiver

Adds a [`CapturedResultReceiver`]({{ site.dcv_flutter_api }}capture-vision-router/captured-result-receiver.html) object as the receiver of captured results.

```dart
Future<void> addResultReceiver(CapturedResultReceiver receiver)
```

### removeAllResultFilters

Removes all the result filters from the Capture Vision Router instance.

```dart
Future<void> removeAllResultFilters()
```

### removeAllResultReceivers

Removes all result receivers from the Capture Vision Router instance.

```dart
Future<void> removeAllResultReceivers()
```

### removeResultFilter

Removes a previously added result filter.

```dart
Future<void> removeResultFilter(MultiFrameResultCrossFilter filter)
```

### removeResultReceiver

Removes a previously added result receiver.

```dart
Future<void> removeResultReceiver(CapturedResultReceiver receiver)
```

### setInput

Sets up an image source to provide images for continuous processing. This method is mainly used when configuring a camera (via the [`CameraEnhancer`]({{ site.dce_flutter_api }}camera-enhancer.html)) as an input source.

```dart
Future<void> setInput(ImageSourceAdapter input) async
```

**Parameters**

`[in] imageSourceAdapter`: An object of [`ImageSourceAdapter`]({{ site.dcv_flutter_api }}core/image-source-adapter.html).

You can use the following officially implemented `ImageSourceAdapter` classes:

- [`CameraEnhancer`]({{ site.dce_flutter_api }}camera-enhancer.html): A camera class that can capture video frames continuously.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

### startCapturing

Starts the capturing process using the specified template. Any result(s) that are received while the capture process is underway will be relayed by a result receiver, which is a callback function that is triggered once a captured result is found.

```dart
Future<void> startCapturing(String templateName)
```

**Parameters**

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

### stopCapturing

Stops the capturing process.

```dart
Future<void> stopCapturing()
```

### switchCapturingTemplate

Switch the image processing settings with the CaptureVisionTemplate name during the image processing workflow.

```dart
Future<void> switchCapturingTemplate(String templateName) async
```

**Parameters**

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |

### getSimplifiedSettings

Returns a subset of the full applied settings as a [`SimplifiedCaptureVisionSettings`](simplified-capture-vision-settings.md) object. This object contains the simplified settings of the Capture Vision Router instance, which in turn contains the simplified settings of the functional product used.

```dart
Future<SimplifiedCaptureVisionSettings?> getSimplifiedSettings(String templateName) async
```

**Parameters**

`[in] templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CONVERT_COMPLEX_TEMPLATE_ERROR | -10061 | The template you specified is a complex template which can not be output as a `SimplifiedCaptureVisionSettings` object. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

### getTemplateNames

Returns all the currently available Capture Vision template names.

```dart
Future<List<String>> getTemplateNames() async
```

### initSettings

Initializes the settings of the `CaptureVisionRouter` instance using a JSON template (as a JSON string). To learn how to use a customized JSON template, please refer to this [section of the Foundational User Guide]({{ site.dbr_flutter }}foundational-user-guide.html#using-a-json-template).

```dart
Future<void> initSettings(String content)
```

**Parameters**

`[in] content`: A JSON string that contains Capture Vision settings.

**Exception**

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

### initSettingsFromFile

Initializes the settings of the `CaptureVisionRouter` instance using a JSON template (as a JSON file). To learn how to use a customized JSON template, please refer to this [section of the Foundational User Guide]({{ site.dbr_flutter }}foundational-user-guide.html#using-a-json-template).

```dart
Future<void> initSettingsFromFile(String filePath) async
```

**Parameters**

`[in] filePath`: A JSON file that contains Capture Vision settings.

**Exception**

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

### outputSettings

Outputs the specified Capture Vision template's settings as a JSON string. If `includeDefaultValues` is set to true, the output will include the default settings values.

```dart
Future<String?> outputSettings(String templateName, bool includeDefaultValues) async
```

**Parameters**

`[in] templateName`: The name of the template that you want to output.

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

`[in] includeDefaultValues`: A boolean value that indicates whether to include default values in the output.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

### outputSettingsToFile

Outputs the specified Capture Vision template's settings to a JSON file. If `includeDefaultValues` is set to true, the output will include the default settings values.

```dart
Future<void> outputSettingsToFile(String templateName, String filePath, bool includeDefaultValues) async
```

**Parameters**

`[in] templateName`: The name of the template that you want to output.

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

`[in] file`: The file path and name that you want to save the template.

`[in] includeDefaultValues`: A boolean value that indicates whether to include default values in the output.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_SAVE_FAILED | -10058 | The file path is unavailable or the file can't be created for any other reasons. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

### resetSettings

Resets all of the settings to their default values.

```dart
Future<void> resetSettings() async
```

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

### updateSettings

Updates the specified template settings of the `CaptureVisionRouter` instance using a [`SimplifiedCaptureVisionSettings`](simplified-capture-vision-settings.md) object. To learn how to update the settings using the SimplifiedCaptureVisionSettings class - please refer to this [section of the Foundational User Guide]({{ site.dbr_flutter }}foundational-user-guide.html#using-simplifiedcapturevisionsettings).

```dart
Future<void> updateSettings(String templateName, SimplifiedCaptureVisionSettings settings)
```

**Parameters**

`[in] templateName`: Specify the name of the template that you want to update.

- One of the [`EnumPresetTemplate`]({{ site.dcv_flutter_api }}core/enum/preset-template.html) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

`[in] settings`: An object of `SimplifiedCaptureVisionSettings`.

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_PARAMETER_VALUE_INVALID | -10038 | There exists invalid parameter value in your `SimplifiedCaptureVisionSettings`. |
| EC_CONVERT_COMPLEX_TEMPLATE_ERROR | -10061 | The template you specified is a complex template which can not be updated via a `SimplifiedCaptureVisionSettings` object. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

### setGlobalIntraOpNumThreads

Sets the global number of threads used internally by the library for model execution. This parameter could help regulate the resources needed to operate the Capture Vision Router instance.

```dart
static Future<void> setGlobalIntraOpNumThreads(int intraOpNumThreads)
```

**Parameters**

`intraOpNumThreads`: Number of threads used internally for model execution. Valid range: [0, 256]. Default: 2.

### clearDLModelBuffers

Clears the buffer used by deep learning models to free up memory and resources used by the Capture Vision Router instance for its operation.

```dart
static Future<void> clearDLModelBuffers()
```

### getIntermediateResultManager

Retrieves the [`IntermediateResultManager`](intermediate-result-manager.md) instance.

```dart
IntermediateResultManager getIntermediateResultManager();
```
