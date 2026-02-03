---
layout: default-layout
title: AuxiliaryRegionElement - Dynamsoft Capture Vision Android Edition API Reference
description: The class AuxiliaryRegionElement of Dynamsoft Capture Vision Android represents an auxiliary region element that contains additional region information detected during processing.
keywords: auxiliary region, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# AuxiliaryRegionElement

The `AuxiliaryRegionElement` class extends the `RegionObjectElement` class and represents an auxiliary region element that contains additional region information detected during processing (e.g., portrait zones, specific document areas).

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class AuxiliaryRegionElement extends RegionObjectElement
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getName`](#getname) | Gets the name of this auxiliary region. |
| [`getConfidence`](#getconfidence) | Gets the confidence level of this auxiliary region detection. |
| [`setName`](#setname) | Sets the name/type of this auxiliary region. |
| [`setLocation`](#setlocation) | Sets the location of this auxiliary region. |
| [`setConfidence`](#setconfidence) | Sets the confidence level of this auxiliary region detection. |

## Inherited Methods

The following methods are inherited from class [`RegionObjectElement`]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html).

| Method | Description |
|------- |-------------|
| [`getLocation`]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html#getlocation) | Gets the location of the region object, represented as a [`Quadrilateral`]({{ site.dcv_android_api }}core/basic-structures/quadrilateral.html). |
| [`getReferencedElement`]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html#getreferencedelement) | Gets the referenced element that supports the capturing of this element. |
| [`getType`]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html#gettype) | Gets the type of the region object element, defined by the enumeration [`EnumRegionObjectElementType`]({{ site.dcv_android_api }}core/enum/region-object-element-type.html). |
| [`getImageData`]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html#getimagedata) | Gets the original image that produce this element. |

### getName

Gets the name of this auxiliary region.

```java
String getName();
```

**Return Value**

A string representing the region name (e.g., "PortraitZone", "SignatureArea").

### getConfidence

Gets the confidence level of this auxiliary region detection.

```java
int getConfidence();
```

**Return Value**

The confidence value, typically in the range [0, 100].

### setName

Sets the name/type of this auxiliary region.

```java
void setName(String name);
```

**Parameters**

`[in] name`: The region name to set (e.g., "PortraitZone", "SignatureArea").

### setLocation

Sets the location of this auxiliary region.

```java
int setLocation(Quadrilateral location);
```

**Parameters**

`[in] location`: A [`Quadrilateral`]({{ site.dcv_android_api }}core/basic-structures/quadrilateral.html) defining the region boundaries.

**Return Value**

Returns 0 if successful, otherwise returns an error code.

### setConfidence

Sets the confidence level of this auxiliary region detection.

```java
void setConfidence(int confidence);
```

**Parameters**

`[in] confidence`: The confidence value to set, typically in the range [0, 100].