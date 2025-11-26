---
layout: default-layout
title: CharacterResult - Dynamsoft Label Recognizer Android Edition
description: The class CharacterResult of Dynamsoft Label Recognizer Android edition represents the result of a character recognition process.
keywords: Character result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CharacterResult
---

# CharacterResult

The `CharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```java
class CharacterResult
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`CharacterH`](#characterh) | Returns the highest confidence character recognized. |
| [`CharacterM`](#characterm) | Returns the medium confidence character recognized. |
| [`CharacterL`](#characterl) | Returns the lowest confidence character recognized. |
| [`Location`](#location) | Returns the location of the recognized character within the image. |
| [`CharacterHConfidence`](#characterhconfidence) | Returns the confidence score for the highest confidence character. |
| [`CharacterMConfidence`](#charactermconfidence) | Returns the confidence score for the medium confidence character. |
| [`CharacterLConfidence`](#characterlconfidence) | Returns the confidence score for the lowest confidence character. |

### CharacterH

Returns the highest confidence character recognized.

```java
String characterH;
```

### CharacterM

Returns the medium confidence character recognized.

```java
String characterM;
```

### CharacterL

Returns the lowest confidence character recognized.

```java
String characterL;
```

### Location

Returns the location of the recognized character within the image.

```java
Quadrilateral? location;
```

### CharacterHConfidence

Returns the confidence score for the highest confidence character.

```java
int characterHConfidence;
```

### CharacterMConfidence

Returns the confidence score for the medium confidence character.

```java
int characterMConfidence;
```

### CharacterLConfidence

Returns the confidence score for the lowest confidence character.

```java
int characterLConfidence;
```
