---
layout: default-layout
Title: CaptureVisionRouterException - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The CaptureVisionRouterException class defines the exceptions of Dynamsoft Capture Vision Router Module.
Keywords: capture state, monitoring, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CaptureVisionRouterException

The CaptureVisionRouterException class defines the exceptions of Dynamsoft Capture Vision Router Module.

## Definition

*Namespace*: com.dynamsoft.cvr
*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
class CaptureVisionRouterException extends Exception
```

## Methods

| Method | Description |
|------- |-------------|
| [`getErrorCode`](#geterrorcode) | Get the error code. |

### getErrorCode

Get the error code.

```java
int getErrorCode();
```

**Return Value**

An int value that indicates the error code. View `EnumErrorCode` for more information.
