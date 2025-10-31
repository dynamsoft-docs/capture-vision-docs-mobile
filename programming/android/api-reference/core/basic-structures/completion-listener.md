---
layout: default-layout
title: CompletionListener - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The interface CompletionListener of Dynamsoft Capture Vision Router Module defines the methods for handling callback when startCapturing is finished.
keywords: startCapturing, completion, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CompletionListener

The `CompletionListener` interface defines methods to receive callback when [`startCapturing`](../../capture-vision-router/multiple-file-processing.html#startcapturing) method is finished.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
interface CompletionListener
```

## Methods

| Method | Description |
|------- |-------------|
| [`onSuccess`](#onsuccess) | The methods is triggered when the `startCapturing` succeed. |
| [`onFailure`](#onfailure) | The methods is triggered when the `startCapturing` failed. |

### onSuccess

The methods is triggered when the `startCapturing` is success.

```java
void onSuccess();
```

### onFailure

The methods is triggered when the `startCapturing` failed.

```java
void onFailure(int errorCode, String errorString);
```

**Parameters**

`[in] errorCode`: The error code that describes why the `startCapturing` failed.

`[in] errorString`: The error message that describes why the `startCapturing` failed.

Possible Errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_LICENSE_INVALID | -10003 | License invalid. |
| EC_LICENSE_EXPIRED | -10004 | License expired. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_LICENSE_KEY_NOT_MATCH | -10043 | The license key does not match the license content. |
| EC_REQUEST_FAILED | -10044 | Failed to request the license content. |
| EC_LICENSE_INIT_FAILED | -10045 | Failed to init the license. |
| EC_LICENSE_CONTENT_INVALID | -10052 | The license content is invalid. |
| EC_LICENSE_KEY_INVALID | -10053 | The license key is invalid. |
| EC_LICENSE_DEVICE_RUNS_OUT | -10054 | The license key has no remaining quota. |
| EC_IRT_LICENSE_INVALID | -10056 | The Intermediate Result Types license is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_NO_IMAGE_SOURCE | -10063 | Can not start capturing before you set the input. |
| EC_NO_LICENSE | -20000 | No license. |
| EC_HANDSHAKE_CODE_INVALID | -20001 | The Handshake Code is invalid. |
| EC_LICENSE_BUFFER_FAILED | -20002 | Failed to read or write license buffer. |
| EC_LICENSE_SYNC_FAILED | -20003 | Failed to synchronize license info with license server. |
| EC_DEVICE_NOT_MATCH | -20004 | Device dose not match with buffer. |
| EC_BIND_DEVICE_FAILED | -20005 | Failed to bind device. |
| EC_INSTANCE_COUNT_OVER_LIMIT | -20008 | Instance count is over limit. |
| EC_TRIAL_LICENSE | -20010 | Trial License. |
| EC_FAILED_TO_REACH_DLS | -20200 | Failed to reach License Server. |
