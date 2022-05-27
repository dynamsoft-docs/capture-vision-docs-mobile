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

The barcode decoding feature of DCV is designed to be excellent on the performance and user-friendly on development. When working with DCV, users can easily deploy image or video barcode decoding functionality in cross-platform applications. Various processing parameters enable users to adjust performance on different usage scenarios. The following paragraphs will provide a brief overview on the barcode decoding feature.

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

<!--
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
-->

## SDK Modules

- `DynamsoftCameraView`: The module that enable users to quickly deploy a camera view to capture and display the video streaming. Users can add basic UI elements on the view to improve the interactivity of the view.
- `DynamsoftBarcodeReader`: The module that supports barcode decoding feature. Users can specify barcode formats, control the start/stop of the barcode decoding thread, obtain barcode decoding results or upload advanced parameter controls via the module.

<!--
- `DynamsoftDocumentNormalizer`: The module that supports document scanning feature. The module includes the boundary detection algorithm and APIs that enable users to configure detection and normalization settings or upload advanced parameter settings.
- `DynamsoftLabelRecognizer`: The module that supports the label text recognition feature. When working with this module, users can improve the performance on localizating the text area or recognizing text by switching the recognition modes, modules and templates.

> Note:
>
> `DynamsoftDocumentNormalizer` and `DynamsoftLabelRecognizer` are not available in 1.0 version.
-->

## Scenarios

### Retail

The following feature of DCV can be applied to retail scenarios:

- Detect the labels on the commodities
- Quickly scan the barcodes on the labels
- Extract and parse the main content of the labels

### Driver's License Recognition

PDF417 symbology is used for storing personal information on US driver licenses. It comprises critical information about the cardholder, such as their name, gender, date of birth, height, etc. With the help of DCV barcode decoding feature, user can easily capture, recognize and parse the driver's information from the PDF417 barcode on mobile devices.

### VIN Scanning

DCV provides multiple solutions on recognizing Vehicle Identification Numbers (VINs). Generally when the VIN is accompanied with a barcode, barcode decoding feature is the highest solution on collecting the VIN data. When the VIN barcode is not available, user can still use the label recognition module to obtain the vehicle information.

## Supported Platforms

| Language | Platform |
| -------- | -------- |
| <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyZpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDcuMS1jMDAwIDc5LjljY2M0ZGU5MywgMjAyMi8wMy8xNC0xNDowNzoyMiAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIDIzLjMgKFdpbmRvd3MpIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOjI0RjY4NjRBREQ4NjExRUNBQUQxQzJGRjA3NzRGNDAxIiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOjI0RjY4NjRCREQ4NjExRUNBQUQxQzJGRjA3NzRGNDAxIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6MjRGNjg2NDhERDg2MTFFQ0FBRDFDMkZGMDc3NEY0MDEiIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6MjRGNjg2NDlERDg2MTFFQ0FBRDFDMkZGMDc3NEY0MDEiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz5bKmoBAAAHSklEQVR42uyY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" alt="rn"> React Native | <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAADm0lEQVRYR82XSyhtURjH/8freBUOAwYSA4RIBpIQBobKhCikyMiAgZSxREomlGIgIykZkgHKQCGPgbylZOKZ9+s4/3XXudexH2efzrq3+6vd2ftba6/zX9/61re+bXO6wH9AgPxVxtnZGaampnByciItFqFHVDE8POwsKytzZmVlOefm5qTVGko88vHxgfr6evT19eHi4gKxsbFISEiQrdZQIqS/vx/Ly8uIiYmBzWZDcnIy0tPTZas1/BZyfn6O6elpREdH4/PzEy8vL6ipqUFQUJDsYQ2/hTAwn56e8P7+jufnZzQ0NKCiokK2WsdvIXt7e7i8vER8fDw6OjrQ3d0tW3zDpzxyf3+PyMhI+fSLxcVFPD4+Ij8/Hw6HQ9gODw8REhKCxMRE8WwFr0K2trYwNDSE1dVV4X52ZyA2NTWhvLwc4eHhYtcsLS1hfHwca2trog+DljFTWlqK1tZWZGdnyxH1MRTy+vqKkZERDA4OIiwsTMyQg5O3tzfhBS5HZmYmDg4OcHx8jIiICNHvO4wfvkcxbW1t0qrFUAi3JGdot9sRGBgorX/ga/QEL7bzcgv9CT15dXWF3t5e1NbWSqsnukLm5+fFDKKiohAQ4F88c3juppycHExOThqK1RVSUlKC6+trjZt9hUMzr7hSPiYmJhAcHCxbtGime3R0JJKU2UtWYbAybuhdb+NphCwsLCgRQW8wNlJTU1FcXCytxmiE7O/vG66jr9AjaWlpluJM0+Pm5kaZEOJOct7QCPF3l/zk7u5O3pmj+VfOQGcj+Qy9ymt3d1dazNEISUpKUiKEMOh57vCY8IZGCM8EZksVcJmZUcfGxqTFGI2QgoIC4VJVyxMaGorZ2Vl0dXWJ7WyEbmTm5eWJQ08FFMMSklVcc3MzdnZ2ZIsnukJYZT08PCiLFYphubC9vY3b21tp9URXCDNhbm6uMq+4sywPvsLCQmn1RFcI17W6ulrMhNlRBaxLWlpa5JMWXSGkqqpKVGI8Pf1ZIr7LZXZ9eIly0gjTUvH09BSVlZXi3tfPA8KhubxxcXGYmZkR9Y0Rhh4hTG7t7e2iLGRu4cDui0vGgocFNS96jrbvffgOk1pnZ6epCGLqETcDAwNwfdf+rlsZePxTujsjI0P0WVlZwfr6ukhi9B7bOYGenh7U1dWJPmZYEkI2NzcxOjoqZllUVKRbe9IrLAc3NjZE7mhsbERKSopsNceykL+NaYz8O4AvmEMyZO/vrSAAAAAASUVORK5CYII=" alt="iOS"> iOS / <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAAEGUlEQVRYR+2XXWwUVRTH/7s7+9HuttuVUmmkFNIC1tgqFAhBYxOj0ugD8Umb+IIJmGiUZ8WYmuiTISEmRvTBB03Kgw/yqeHNj1gSPwIUorRViy0Y2nTb3Xa/ZnZmx3Pu3KVlnaV32ho18ddMd+6dO/f+77nnnnvGZxP4F+CXv/84noSYtolzowOyVJ2p7A1c+OMbWVLDkxDNpyEWjmN4+qIoZ4vzuDE3hon0L5jMXIdZKor6y5PnkahtEveqLMtHjn3/BmLBOvyWuoqMnkKJ/oL+EOrDd6F9zf2IBuN4cstzsrUanoSU7BI+vfIePh/9RAzs9wXocozKndi2RVYxUROMoa/rEB7e8JR4poInIR/+0I9vx7+gmSdg0YCMz+cTv4xNQn1SWEZP4/nuw+jZuE+Ul0LZR85PnMMgiSiRgCN7T2Jb8yMolgz51KFg5tHXeQgv7HyTLORYjx1XBWWLvHK2F7pVoFnb6GjqFk6aNdJiecqwlZpiLQhrEYynRkhoEbvveRwHd/bLFtVRssjQzUEYli4GDQZC+Hnqx7+IYAJ+DVOZCSFC8wfJj4L4PT2M6dxN2aI6SkJGkheQMeagk+kLxZyYuWHq4r7yKloGTKso73Xa2qOYzU3KnqqjtDSXJgcxNvOTmKVXdCuPntZ9aIw2yxp3XIWMp0dwfOhdJGoacXBHP76+dpqC1CAtS1i2UCdfzOKZzpfJ9H4MDB2l5QvgxV1vi2VcjKuQl848Rh3kyMQGnmh/FuFgLU5d/QgRrVa2UGeeAt6R3hN466sDYmnZgR/d9DT2b39NtnBw9ZEciQhrNQjRZdBO4eAVImss9+LZs+9EqL8wlfNmVo60gKuQcrTkWFUOUCvF6YeDn+9W/4tZnVFWgf+FVPLfECL2tdpRpEC5H9u1yzsIodb0Br/j/F8ZHK74RK6Gq5DtdMTP5KconmSwu2WviAErgWMRJ0mpfJLOrDQeWPeQfLKAa2TlLGs0eQkNkUY017Xi44vv4Muxz0RkXZwILQV3PafP4nDPB+hYuwO/Jq8gENCwseFe2WIBV4toFAk71nYLEcy66HqRBM0bs7cSZIZTRw7hfGWNeVnrUDBzmKP20VAdaim/Zdoon3UTwSidvnxGXKNEORSIYODyUco3hp1chN58tecYnUsZpApJvP/d62JgFtHb3ocHaYk5xLfUt8NPh92dUNq+fO5sbdyGTYkOxEL1whIONjbEN4tn95HpTZk6cr6yPt6GzWu60NqwdUkRjJKQxSyIuH03VTo0+5kXPAu5bSUrFnUl29yzEMYih+VPhxJ9x5RhEU5dCRbVexXlWQg7YTQUR1qfQVfzHlkL8SnaefcepAvTwm/aEp3yiRpKu6YSfoWjZGUWz7CV3OqXYllC/g6W5SOrD/AnZ/TjX8xYY2sAAAAASUVORK5CYII=" alt="android"> Android |
| <img src="data:image/jpeg;base64,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" alt="flutter"> Flutter | <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAADm0lEQVRYR82XSyhtURjH/8freBUOAwYSA4RIBpIQBobKhCikyMiAgZSxREomlGIgIykZkgHKQCGPgbylZOKZ9+s4/3XXudexH2efzrq3+6vd2ftba6/zX9/61re+bXO6wH9AgPxVxtnZGaampnByciItFqFHVDE8POwsKytzZmVlOefm5qTVGko88vHxgfr6evT19eHi4gKxsbFISEiQrdZQIqS/vx/Ly8uIiYmBzWZDcnIy0tPTZas1/BZyfn6O6elpREdH4/PzEy8vL6ipqUFQUJDsYQ2/hTAwn56e8P7+jufnZzQ0NKCiokK2WsdvIXt7e7i8vER8fDw6OjrQ3d0tW3zDpzxyf3+PyMhI+fSLxcVFPD4+Ij8/Hw6HQ9gODw8REhKCxMRE8WwFr0K2trYwNDSE1dVV4X52ZyA2NTWhvLwc4eHhYtcsLS1hfHwca2trog+DljFTWlqK1tZWZGdnyxH1MRTy+vqKkZERDA4OIiwsTMyQg5O3tzfhBS5HZmYmDg4OcHx8jIiICNHvO4wfvkcxbW1t0qrFUAi3JGdot9sRGBgorX/ga/QEL7bzcgv9CT15dXWF3t5e1NbWSqsnukLm5+fFDKKiohAQ4F88c3juppycHExOThqK1RVSUlKC6+trjZt9hUMzr7hSPiYmJhAcHCxbtGime3R0JJKU2UtWYbAybuhdb+NphCwsLCgRQW8wNlJTU1FcXCytxmiE7O/vG66jr9AjaWlpluJM0+Pm5kaZEOJOct7QCPF3l/zk7u5O3pmj+VfOQGcj+Qy9ymt3d1dazNEISUpKUiKEMOh57vCY8IZGCM8EZksVcJmZUcfGxqTFGI2QgoIC4VJVyxMaGorZ2Vl0dXWJ7WyEbmTm5eWJQ08FFMMSklVcc3MzdnZ2ZIsnukJYZT08PCiLFYphubC9vY3b21tp9URXCDNhbm6uMq+4sywPvsLCQmn1RFcI17W6ulrMhNlRBaxLWlpa5JMWXSGkqqpKVGI8Pf1ZIr7LZXZ9eIly0gjTUvH09BSVlZXi3tfPA8KhubxxcXGYmZkR9Y0Rhh4hTG7t7e2iLGRu4cDui0vGgocFNS96jrbvffgOk1pnZ6epCGLqETcDAwNwfdf+rlsZePxTujsjI0P0WVlZwfr6ukhi9B7bOYGenh7U1dWJPmZYEkI2NzcxOjoqZllUVKRbe9IrLAc3NjZE7mhsbERKSopsNceykL+NaYz8O4AvmEMyZO/vrSAAAAAASUVORK5CYII=" alt="iOS"> iOS / <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAiCAYAAAA6RwvCAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAACXBIWXMAAA7EAAAOxAGVKw4bAAAABmJLR0QAAAAAAAD5Q7t/AAAEGUlEQVRYR+2XXWwUVRTH/7s7+9HuttuVUmmkFNIC1tgqFAhBYxOj0ugD8Umb+IIJmGiUZ8WYmuiTISEmRvTBB03Kgw/yqeHNj1gSPwIUorRViy0Y2nTb3Xa/ZnZmx3Pu3KVlnaV32ho18ddMd+6dO/f+77nnnnvGZxP4F+CXv/84noSYtolzowOyVJ2p7A1c+OMbWVLDkxDNpyEWjmN4+qIoZ4vzuDE3hon0L5jMXIdZKor6y5PnkahtEveqLMtHjn3/BmLBOvyWuoqMnkKJ/oL+EOrDd6F9zf2IBuN4cstzsrUanoSU7BI+vfIePh/9RAzs9wXocozKndi2RVYxUROMoa/rEB7e8JR4poInIR/+0I9vx7+gmSdg0YCMz+cTv4xNQn1SWEZP4/nuw+jZuE+Ul0LZR85PnMMgiSiRgCN7T2Jb8yMolgz51KFg5tHXeQgv7HyTLORYjx1XBWWLvHK2F7pVoFnb6GjqFk6aNdJiecqwlZpiLQhrEYynRkhoEbvveRwHd/bLFtVRssjQzUEYli4GDQZC+Hnqx7+IYAJ+DVOZCSFC8wfJj4L4PT2M6dxN2aI6SkJGkheQMeagk+kLxZyYuWHq4r7yKloGTKso73Xa2qOYzU3KnqqjtDSXJgcxNvOTmKVXdCuPntZ9aIw2yxp3XIWMp0dwfOhdJGoacXBHP76+dpqC1CAtS1i2UCdfzOKZzpfJ9H4MDB2l5QvgxV1vi2VcjKuQl848Rh3kyMQGnmh/FuFgLU5d/QgRrVa2UGeeAt6R3hN466sDYmnZgR/d9DT2b39NtnBw9ZEciQhrNQjRZdBO4eAVImss9+LZs+9EqL8wlfNmVo60gKuQcrTkWFUOUCvF6YeDn+9W/4tZnVFWgf+FVPLfECL2tdpRpEC5H9u1yzsIodb0Br/j/F8ZHK74RK6Gq5DtdMTP5KconmSwu2WviAErgWMRJ0mpfJLOrDQeWPeQfLKAa2TlLGs0eQkNkUY017Xi44vv4Muxz0RkXZwILQV3PafP4nDPB+hYuwO/Jq8gENCwseFe2WIBV4toFAk71nYLEcy66HqRBM0bs7cSZIZTRw7hfGWNeVnrUDBzmKP20VAdaim/Zdoon3UTwSidvnxGXKNEORSIYODyUco3hp1chN58tecYnUsZpApJvP/d62JgFtHb3ocHaYk5xLfUt8NPh92dUNq+fO5sbdyGTYkOxEL1whIONjbEN4tn95HpTZk6cr6yPt6GzWu60NqwdUkRjJKQxSyIuH03VTo0+5kXPAu5bSUrFnUl29yzEMYih+VPhxJ9x5RhEU5dCRbVexXlWQg7YTQUR1qfQVfzHlkL8SnaefcepAvTwm/aEp3yiRpKu6YSfoWjZGUWz7CV3OqXYllC/g6W5SOrD/AnZ/TjX8xYY2sAAAAASUVORK5CYII=" alt="android"> Android |
