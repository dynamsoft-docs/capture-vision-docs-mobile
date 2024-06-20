---
layout: default-layout
title: CoreException - Dynamsoft Capture Vision MAUI API Reference
description: The class CoreException of DCV MAUI defines the exceptions of Dynamsoft Capture Vision.
keywords: exception
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CoreException

The `CoreException` class defines the exceptions of Dynamsoft Capture Vision.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
class CoreException:Exception
```

## Methods & Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`ErrorCode`](#errorcode) | *int* | Get the error code. |
| [`ErrorMessage`](#errormessage) | *string* | Get the error message. |

| Method | Description |
| ------ |-------------|
| [`CoreException`](#coreexception) | The constructor. |

### ErrorCode

Get the error code.

```csharp
int ErrorCode { get; }
```

### ErrorMessage

Get the error message.

```csharp
string ErrorMessage { get; }
```

### CoreException

The constructor.

```csharp
CoreException(int errorCode, string errorMessage);
```
