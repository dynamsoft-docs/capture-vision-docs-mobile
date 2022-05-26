---
layout: default-layout
title: Dynamsoft Capture Vision - Introduction
description: This is the Introduction Page of Dynamsoft Capture Vision.
keywords:  Capture Vision, Introduction
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
breadcrumbText: Introduction
---

# Introduction to Dynamsoft Capture Vision

Dynamsoft Capture Vision (DCV) is an SDK designed for users to quickly embed barcode decoding, document scanning and label text recognizing features to a cross-platform application. A build-in camera view is available for users to capture and display the video streaming for image processing.

## Key Features

### Barcode Decoding

DCV barcode reading feature enables users to scan barcodes from static images or video streaming.

#### Supported Barcode Symbologies

DCV supports all the common barcode symbologies which cover the majority of industries such as retail, commodity, drivers' license, etc. As for 1.0 version, the following barcode symbologies are supported:

| 1D/Linear Barcodes       | 2D Barcodes         | GS1 DataBar             | Postal Codes          | Other Types        |
|--------------------------|---------------------|-------------------------| --------------------- | ------------------ |
| Code 39/Code 39 Extended | QR Code             | Omnidirectional         | USPS Intelligent Mail | GS1 Composite Code |
| Code 93                  | Micro QR Code       | Truncated               | Postnet               | Patch Code         |
| Code 128                 | Data Matrix         | Stacked                 | Planet                | Pharmacode         |
| Codabar                  | PDF417              | Stacked Omnidirectional | Australian Post       |                    |
| Interleaved 2 of 5       | Micro PDF417        | Limited                 | UK Royal Mail         |                    |
| EAN-8                    | Aztec Code          | Expanded                |                       |                    |
| EAN-13                   | MaxiCode (mode 2-5) | Expanded Stacked        |                       |                    |
| UPC-A                    | DotCode             |                         |                       |                    |
| UPC-E                    |                     |                         |                       |                    |
| Industrial 2 of 5        |                     |                         |                       |                    |
| MSI (Modified Plessey)   |                     |                         |                       |                    |
| Code 11                  |                     |                         |                       |                    |

#### Performance

- Speed: DCV is able to scan 500+ barcodes per minutes.
- Read Rate: DCV can easily recognize the barcode even if they are curved, wrinkled, incompleted. The challenging environments like dark, shadowed or glaring can also be overcome.
- Accuracy: The decoded barcode results are evaluated and filtered before output. Users can add additional filter conditions to make the output result even more accurate.

#### Basic UI Interaction

When work with DCV, there are some build-in UI elements can help users to improve the interactivity of the barcode scanning applications. For example, user can easily highlight the decoded barcodes on the camera view.

<div align="center">
   <p><img src="assets/highlight-barcode.gif" alt="barcode" width="25%" /></p>
   <p>Highlight Barcodes</p>
</div>

### Document Scanning

DCV can detect quad areas such as the boundaries of document pages and tables from images, and perform document normalization on the images in the detected quads. The detectable areas include but are not limited to:

- Document pages
- Tables
- Cards like ID cards

The normalization process includes:

- Boundary cropping
- Deskew processing

<div align="center">
   <p><img src="assets/dce-ddn-view.gif" alt="DCE CameraView and ImageEditorView" width="25%" /></p>
   <p>Detect and Normalize the Documents</p>
</div>

The following attributes of the output image can be adjusted:

- Colour mode
- Contrast
- Brightness

### Label Recognizing

The label recognizing feature of DCV is designed to extract text areas from an image and recognize the extracted characters. Different from the traditional OCR, DLR algorithm is specified on the symbolized text areas such as:

- Price tags
- Inventory labels
- VIN code
- Driver license
- Passport or Visa MRZ
- ID cards

Models, modes and templates are available to improve the recognition rate.

## SDK Modules

- `DynamsoftCameraView`: The module that enable users to quickly deploy a camera view to capture and display the video streaming. Users can add basic UI elements on the view to improve the interactivity of the view.
- `DynamsoftBarcodeReader`: The module that supports barcode decoding feature. Users can specify barcode formats, control the start/stop of the barcode decoding thread, obtain barcode decoding results or upload advanced parameter controls via the module.
- `DynamsoftDocumentNormalizer`: The module that supports document scanning feature. The module includes the boundary detection algorithm and APIs that enable users to configure detection and normalization settings or upload advanced parameter settings.
- `DynamsoftLabelRecognizer`: The module that supports the label text recognition feature. When working with this module, users can improve the performance on localizating the text area or recognizing text by switching the recognition modes, modules and templates.

> Note:
>
> `DynamsoftDocumentNormalizer` and `DynamsoftLabelRecognizer` are not available in 1.0 version.

## Scenarios

### Retail

The following feature of DCV can be applied to retail scenarios:

- Detect the labels on the commodities
- Quickly scan the barcodes on the labels
- Extract and parse the main content of the labels

### Driver's License Recognition

- If there is a barcode on the Driver's license, DCV can recognize and parse the driver's info via the barcode decode result.
- For the driver's licenses without barcodes, DCV can locate, recognize and extract the driver's info directly from the text info.

### VIN Scanning

DCV provides multiple solutions on recognizing Vehicle Identification Numbers (VINs). Generally when the VIN is accompanied with a barcode, barcode decoding feature is the highest solution on collecting the VIN data. When the VIN barcode is not available, user can still use the label recognition module to obtain the vehicle information.

## Programming

| Language | Platform |
| -------- | -------- |
| React Native | <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAADm0lEQVRYR82XSyhtURjH/8freBUOAwYSA4RIBpIQBobKhCikyMiAgZSxREomlGIgIykZkgHKQCGPgbylZOKZ9+s4/3XXudexH2efzrq3+6vd2ftba6/zX9/61re+bXO6wH9AgPxVxtnZGaampnByciItFqFHVDE8POwsKytzZmVlOefm5qTVGko88vHxgfr6evT19eHi4gKxsbFISEiQrdZQIqS/vx/Ly8uIiYmBzWZDcnIy0tPTZas1/BZyfn6O6elpREdH4/PzEy8vL6ipqUFQUJDsYQ2/hTAwn56e8P7+jufnZzQ0NKCiokK2WsdvIXt7e7i8vER8fDw6OjrQ3d0tW3zDpzxyf3+PyMhI+fSLxcVFPD4+Ij8/Hw6HQ9gODw8REhKCxMRE8WwFr0K2trYwNDSE1dVV4X52ZyA2NTWhvLwc4eHhYtcsLS1hfHwca2trog+DljFTWlqK1tZWZGdnyxH1MRTy+vqKkZERDA4OIiwsTMyQg5O3tzfhBS5HZmYmDg4OcHx8jIiICNHvO4wfvkcxbW1t0qrFUAi3JGdot9sRGBgorX/ga/QEL7bzcgv9CT15dXWF3t5e1NbWSqsnukLm5+fFDKKiohAQ4F88c3juppycHExOThqK1RVSUlKC6+trjZt9hUMzr7hSPiYmJhAcHCxbtGime3R0JJKU2UtWYbAybuhdb+NphCwsLCgRQW8wNlJTU1FcXCytxmiE7O/vG66jr9AjaWlpluJM0+Pm5kaZEOJOct7QCPF3l/zk7u5O3pmj+VfOQGcj+Qy9ymt3d1dazNEISUpKUiKEMOh57vCY8IZGCM8EZksVcJmZUcfGxqTFGI2QgoIC4VJVyxMaGorZ2Vl0dXWJ7WyEbmTm5eWJQ08FFMMSklVcc3MzdnZ2ZIsnukJYZT08PCiLFYphubC9vY3b21tp9URXCDNhbm6uMq+4sywPvsLCQmn1RFcI17W6ulrMhNlRBaxLWlpa5JMWXSGkqqpKVGI8Pf1ZIr7LZXZ9eIly0gjTUvH09BSVlZXi3tfPA8KhubxxcXGYmZkR9Y0Rhh4hTG7t7e2iLGRu4cDui0vGgocFNS96jrbvffgOk1pnZ6epCGLqETcDAwNwfdf+rlsZePxTujsjI0P0WVlZwfr6ukhi9B7bOYGenh7U1dWJPmZYEkI2NzcxOjoqZllUVKRbe9IrLAc3NjZE7mhsbERKSopsNceykL+NaYz8O4AvmEMyZO/vrSAAAAAASUVORK5CYII=" alt="iOS"> iOS / <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAAEGUlEQVRYR+2XXWwUVRTH/7s7+9HuttuVUmmkFNIC1tgqFAhBYxOj0ugD8Umb+IIJmGiUZ8WYmuiTISEmRvTBB03Kgw/yqeHNj1gSPwIUorRViy0Y2nTb3Xa/ZnZmx3Pu3KVlnaV32ho18ddMd+6dO/f+77nnnnvGZxP4F+CXv/84noSYtolzowOyVJ2p7A1c+OMbWVLDkxDNpyEWjmN4+qIoZ4vzuDE3hon0L5jMXIdZKor6y5PnkahtEveqLMtHjn3/BmLBOvyWuoqMnkKJ/oL+EOrDd6F9zf2IBuN4cstzsrUanoSU7BI+vfIePh/9RAzs9wXocozKndi2RVYxUROMoa/rEB7e8JR4poInIR/+0I9vx7+gmSdg0YCMz+cTv4xNQn1SWEZP4/nuw+jZuE+Ul0LZR85PnMMgiSiRgCN7T2Jb8yMolgz51KFg5tHXeQgv7HyTLORYjx1XBWWLvHK2F7pVoFnb6GjqFk6aNdJiecqwlZpiLQhrEYynRkhoEbvveRwHd/bLFtVRssjQzUEYli4GDQZC+Hnqx7+IYAJ+DVOZCSFC8wfJj4L4PT2M6dxN2aI6SkJGkheQMeagk+kLxZyYuWHq4r7yKloGTKso73Xa2qOYzU3KnqqjtDSXJgcxNvOTmKVXdCuPntZ9aIw2yxp3XIWMp0dwfOhdJGoacXBHP76+dpqC1CAtS1i2UCdfzOKZzpfJ9H4MDB2l5QvgxV1vi2VcjKuQl848Rh3kyMQGnmh/FuFgLU5d/QgRrVa2UGeeAt6R3hN466sDYmnZgR/d9DT2b39NtnBw9ZEciQhrNQjRZdBO4eAVImss9+LZs+9EqL8wlfNmVo60gKuQcrTkWFUOUCvF6YeDn+9W/4tZnVFWgf+FVPLfECL2tdpRpEC5H9u1yzsIodb0Br/j/F8ZHK74RK6Gq5DtdMTP5KconmSwu2WviAErgWMRJ0mpfJLOrDQeWPeQfLKAa2TlLGs0eQkNkUY017Xi44vv4Muxz0RkXZwILQV3PafP4nDPB+hYuwO/Jq8gENCwseFe2WIBV4toFAk71nYLEcy66HqRBM0bs7cSZIZTRw7hfGWNeVnrUDBzmKP20VAdaim/Zdoon3UTwSidvnxGXKNEORSIYODyUco3hp1chN58tecYnUsZpApJvP/d62JgFtHb3ocHaYk5xLfUt8NPh92dUNq+fO5sbdyGTYkOxEL1whIONjbEN4tn95HpTZk6cr6yPt6GzWu60NqwdUkRjJKQxSyIuH03VTo0+5kXPAu5bSUrFnUl29yzEMYih+VPhxJ9x5RhEU5dCRbVexXlWQg7YTQUR1qfQVfzHlkL8SnaefcepAvTwm/aEp3yiRpKu6YSfoWjZGUWz7CV3OqXYllC/g6W5SOrD/AnZ/TjX8xYY2sAAAAASUVORK5CYII=" alt="android"> Android |
| Flutter | <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAADm0lEQVRYR82XSyhtURjH/8freBUOAwYSA4RIBpIQBobKhCikyMiAgZSxREomlGIgIykZkgHKQCGPgbylZOKZ9+s4/3XXudexH2efzrq3+6vd2ftba6/zX9/61re+bXO6wH9AgPxVxtnZGaampnByciItFqFHVDE8POwsKytzZmVlOefm5qTVGko88vHxgfr6evT19eHi4gKxsbFISEiQrdZQIqS/vx/Ly8uIiYmBzWZDcnIy0tPTZas1/BZyfn6O6elpREdH4/PzEy8vL6ipqUFQUJDsYQ2/hTAwn56e8P7+jufnZzQ0NKCiokK2WsdvIXt7e7i8vER8fDw6OjrQ3d0tW3zDpzxyf3+PyMhI+fSLxcVFPD4+Ij8/Hw6HQ9gODw8REhKCxMRE8WwFr0K2trYwNDSE1dVV4X52ZyA2NTWhvLwc4eHhYtcsLS1hfHwca2trog+DljFTWlqK1tZWZGdnyxH1MRTy+vqKkZERDA4OIiwsTMyQg5O3tzfhBS5HZmYmDg4OcHx8jIiICNHvO4wfvkcxbW1t0qrFUAi3JGdot9sRGBgorX/ga/QEL7bzcgv9CT15dXWF3t5e1NbWSqsnukLm5+fFDKKiohAQ4F88c3juppycHExOThqK1RVSUlKC6+trjZt9hUMzr7hSPiYmJhAcHCxbtGime3R0JJKU2UtWYbAybuhdb+NphCwsLCgRQW8wNlJTU1FcXCytxmiE7O/vG66jr9AjaWlpluJM0+Pm5kaZEOJOct7QCPF3l/zk7u5O3pmj+VfOQGcj+Qy9ymt3d1dazNEISUpKUiKEMOh57vCY8IZGCM8EZksVcJmZUcfGxqTFGI2QgoIC4VJVyxMaGorZ2Vl0dXWJ7WyEbmTm5eWJQ08FFMMSklVcc3MzdnZ2ZIsnukJYZT08PCiLFYphubC9vY3b21tp9URXCDNhbm6uMq+4sywPvsLCQmn1RFcI17W6ulrMhNlRBaxLWlpa5JMWXSGkqqpKVGI8Pf1ZIr7LZXZ9eIly0gjTUvH09BSVlZXi3tfPA8KhubxxcXGYmZkR9Y0Rhh4hTG7t7e2iLGRu4cDui0vGgocFNS96jrbvffgOk1pnZ6epCGLqETcDAwNwfdf+rlsZePxTujsjI0P0WVlZwfr6ukhi9B7bOYGenh7U1dWJPmZYEkI2NzcxOjoqZllUVKRbe9IrLAc3NjZE7mhsbERKSopsNceykL+NaYz8O4AvmEMyZO/vrSAAAAAASUVORK5CYII=" alt="iOS"> iOS / <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAAEGUlEQVRYR+2XXWwUVRTH/7s7+9HuttuVUmmkFNIC1tgqFAhBYxOj0ugD8Umb+IIJmGiUZ8WYmuiTISEmRvTBB03Kgw/yqeHNj1gSPwIUorRViy0Y2nTb3Xa/ZnZmx3Pu3KVlnaV32ho18ddMd+6dO/f+77nnnnvGZxP4F+CXv/84noSYtolzowOyVJ2p7A1c+OMbWVLDkxDNpyEWjmN4+qIoZ4vzuDE3hon0L5jMXIdZKor6y5PnkahtEveqLMtHjn3/BmLBOvyWuoqMnkKJ/oL+EOrDd6F9zf2IBuN4cstzsrUanoSU7BI+vfIePh/9RAzs9wXocozKndi2RVYxUROMoa/rEB7e8JR4poInIR/+0I9vx7+gmSdg0YCMz+cTv4xNQn1SWEZP4/nuw+jZuE+Ul0LZR85PnMMgiSiRgCN7T2Jb8yMolgz51KFg5tHXeQgv7HyTLORYjx1XBWWLvHK2F7pVoFnb6GjqFk6aNdJiecqwlZpiLQhrEYynRkhoEbvveRwHd/bLFtVRssjQzUEYli4GDQZC+Hnqx7+IYAJ+DVOZCSFC8wfJj4L4PT2M6dxN2aI6SkJGkheQMeagk+kLxZyYuWHq4r7yKloGTKso73Xa2qOYzU3KnqqjtDSXJgcxNvOTmKVXdCuPntZ9aIw2yxp3XIWMp0dwfOhdJGoacXBHP76+dpqC1CAtS1i2UCdfzOKZzpfJ9H4MDB2l5QvgxV1vi2VcjKuQl848Rh3kyMQGnmh/FuFgLU5d/QgRrVa2UGeeAt6R3hN466sDYmnZgR/d9DT2b39NtnBw9ZEciQhrNQjRZdBO4eAVImss9+LZs+9EqL8wlfNmVo60gKuQcrTkWFUOUCvF6YeDn+9W/4tZnVFWgf+FVPLfECL2tdpRpEC5H9u1yzsIodb0Br/j/F8ZHK74RK6Gq5DtdMTP5KconmSwu2WviAErgWMRJ0mpfJLOrDQeWPeQfLKAa2TlLGs0eQkNkUY017Xi44vv4Muxz0RkXZwILQV3PafP4nDPB+hYuwO/Jq8gENCwseFe2WIBV4toFAk71nYLEcy66HqRBM0bs7cSZIZTRw7hfGWNeVnrUDBzmKP20VAdaim/Zdoon3UTwSidvnxGXKNEORSIYODyUco3hp1chN58tecYnUsZpApJvP/d62JgFtHb3ocHaYk5xLfUt8NPh92dUNq+fO5sbdyGTYkOxEL1whIONjbEN4tn95HpTZk6cr6yPt6GzWu60NqwdUkRjJKQxSyIuH03VTo0+5kXPAu5bSUrFnUl29yzEMYih+VPhxJ9x5RhEU5dCRbVexXlWQg7YTQUR1qfQVfzHlkL8SnaefcepAvTwm/aEp3yiRpKu6YSfoWjZGUWz7CV3OqXYllC/g6W5SOrD/AnZ/TjX8xYY2sAAAAASUVORK5CYII=" alt="android"> Android |
