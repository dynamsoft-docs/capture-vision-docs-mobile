---
layout: default-layout
title: DSTextZonesUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSTextZonesUnit of Dynamsoft Core Module represents a unit that contains text zones, which is derived from DSIntermediateResultUnit class.
keywords: text zones unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextZonesUnit

The `DSTextZonesUnit` class extends the `DSIntermediateResultUnit` class and represents a unit of text zones identified during the processing of an image. This class is used to encapsulate the locations of detected text areas within an image, providing a structured representation of where text is located.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSTextZonesUnit: DSIntermediateResultUnit
```
2. 
```swift
class TextZonesUnit: IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`getTextZones`](#gettextzones) | Gets an array of [`DSTextZone`](text-zone.md) objects, each representing the geometric boundaries of a detected text zone within the image. |
| [`getCount`](#getcount) | Returns the number of text zones in this unit. |
| [`getTextZone`](#gettextzone) | Returns the text zone at the specified index. |
| [`removeTextZone`](#removetextzone) | Removes the text zone at the specified index. |
| [`addTextZone`](#addtextzone) | Adds a text zone to this unit. |
| [`setTextZone`](#settextzone) | Sets the text zone at the specified index. |

## Inherited Methods

The following methods are inherited from class [`DSIntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`getHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image associated with this unit. |
| [`getOriginalImageTag`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the tag associated with the original image. |
| [`getType`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=objc,swift). |
| [`getTransformMatrix`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`clone`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`replace`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the content of the intermediate result unit. |

### getTextZones

Gets an array of [`DSTextZone`](text-zone.md) objects, each representing the geometric boundaries of a detected text zone within the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSTextZone*>*)getTextZones;
```
2. 
```swift
func getTextZones() -> [TextZone]?
```

**Return Value**

An array of `DSTextZone` objects.

### getCount

Returns the number of text zones in this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getCount;
```
2. 
```swift
func getCount() -> Int
```

**Return Value**

The number of text zones.

### getTextZone

Returns the text zone at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSTextZone*)getTextZone:(NSInteger)index;
```
2. 
```swift
func getTextZone(index: Int) -> TextZone?
```

**Parameters**

`index`: The index of the text zone.

**Return Value**

Returns the text zone at the specified index.

### removeTextZone

Removes the text zone at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeTextZone:(NSInteger)index;
```
2. 
```swift
func removeTextZone(index: Int)
```

**Parameters**

`index`: The index of the text zone to be removed.

### addTextZone

Adds a text zone to this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addTextZone:(DSTextZone*)textZone
    matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addTextZone(_ textZone: TextZone, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`textZone`: The text zone to be added.

`matrixToOriginalImage`: The transformation matrix from the original image to the text zone.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setTextZone

Sets the text zone at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setTextZone:(NSInteger)index
               textZone:(DSTextZone*)textZone
    matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setTextZone(index: Int, textZone: TextZone, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: The index of the text zone.

`textZone`: The text zone to be set.

`matrixToOriginalImage`: The transformation matrix from the original image to the text zone.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
