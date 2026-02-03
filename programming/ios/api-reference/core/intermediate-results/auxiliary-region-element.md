---
layout: default-layout
title: DSAuxiliaryRegionElement - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSAuxiliaryRegionElement of Dynamsoft Capture Vision iOS represents an auxiliary region element that contains additional region information detected during processing.
keywords: auxiliary region, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSAuxiliaryRegionElement

The `DSAuxiliaryRegionElement` class extends the `DSRegionObjectElement` class and represents an auxiliary region element that contains additional region information detected during processing (e.g., portrait zones, specific document areas).

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSAuxiliaryRegionElement : DSRegionObjectElement
```
2. 
```swift
class AuxiliaryRegionElement : RegionObjectElement
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

The following methods are inherited from class [`DSRegionObjectElement`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html).

| Method | Description |
|------- |-------------|
| [`getLocation`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#getlocation) | Gets the location of the region object, represented as a [`Quadrilateral`]({{ site.dcv_ios_api }}core/basic-structures/quadrilateral.html). |
| [`getReferencedElement`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#getreferencedelement) | Gets the referenced element that supports the capturing of this element. |
| [`getRegionObjectElementType`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#getregionobjectelementtype) | Gets the type of the region object element, defined by the enumeration [`DSRegionObjectElementType`]({{ site.dcv_ios_api }}core/enum/region-object-element-type.html?lang=objc,swift). |
| [`getImageData`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#getimagedata) | Gets the original image that produce this element. |

### getName

Gets the name of this auxiliary region.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSString *)getName;
```
2. 
```swift
func getName() -> String
```

**Return Value**

A string representing the region name (e.g., "PortraitZone", "SignatureArea").

### getConfidence

Gets the confidence level of this auxiliary region detection.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getConfidence;
```
2. 
```swift
func getConfidence() -> Int
```

**Return Value**

The confidence value, typically in the range [0, 100].

### setName

Sets the name/type of this auxiliary region.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setName:(NSString *)name;
```
2. 
```swift
func setName(_ name: String)
```

**Parameters**

`name`: The region name to set (e.g., "PortraitZone", "SignatureArea").

### setLocation

Sets the location of this auxiliary region.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)setLocation:(DSQuadrilateral *)location;
```
2. 
```swift
func setLocation(_ location: Quadrilateral?) -> Int
```

**Parameters**

`location`: A [`DSQuadrilateral`]({{ site.dcv_ios_api }}core/basic-structures/quadrilateral.html) defining the region boundaries.

**Return Value**

Returns 0 if successful, otherwise returns an error code.

### setConfidence

Sets the confidence level of this auxiliary region detection.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setConfidence:(NSInteger)confidence;
```
2. 
```swift
func setConfidence(_ confidence: Int)
```

**Parameters**

`confidence`: The confidence value to set, typically in the range [0, 100].
