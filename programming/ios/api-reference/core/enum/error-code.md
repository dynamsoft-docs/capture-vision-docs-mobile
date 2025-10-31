---
layout: default-layout
title: ErrorCode - Dynamsoft Core Enumerations
description: The enumeration ErrorCode of Dynamsoft Core describes all error codes.
keywords: Error code
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ErrorCode
codeAutoHeight: true
---

# Enumeration ErrorCode

`ErrorCode` enumerates the specific error codes that the SDK may return, providing a systematic way to identify and handle errors encountered during its operation.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ERROR_ENUM(DSErrorDomain, DSError) {
   /**Successful. */
   DSErrorOK                               = 0,
   /**Unknown error. */
   DSErrorUnknown                          = -10000,
   /**Not enough memory to perform the operation. */
   DSErrorNoMemory                         = -10001,
   /**Null pointer */
   DSErrorNullPointer                      = -10002,
   /**License invalid*/
   DSErrorLicenseInvalid                   = -10003,
   /**License expired*/
   DSErrorLicenseExpired                   = -10004,
   /**File not found*/
   DSErrorFileNotFound                     = -10005,
   /**The file type is not supported. */
   DSErrorFiletypeNotSupported             = -10006,
   /**The BPP (Bits Per Pixel) is not supported. */
   DSErrorBPPNotSupported                  = -10007,
   /**Failed to read the image. */
   DSErrorImageReadFailed                  = -10012,
   /**Failed to read the TIFF image. */
   DSErrorTiffReadFailed                   = -10013,
   /**The DIB (Device-Independent Bitmaps) buffer is invalid. */
   DSErrorDIBBufferInvalid                 = -10018,
   /**Failed to read the PDF image. */
   DSErrorPdfReadFailed                    = -10021,
   /**The PDF DLL is missing. */
   DSErrorPdfDllMissing                    = -10022,
   /**The page number is invalid. */
   DSErrorPageNumberInvalid                = -10023,
   /**The custom size is invalid. */
   DSErrorCustomSizeInvalid                = -10024,
   /** timeout. */
   DSErrorTimeout                          = -10026,
   /**Json parse failed*/
   DSErrorJsonParseFailed                  = -10030,
   /**Json type invalid*/
   DSErrorJsonTypeInvalid                  = -10031,
   /**Json key invalid*/
   DSErrorJsonKeyInvalid                   = -10032,
   /**Json value invalid*/
   DSErrorJsonValueInvalid                 = -10033,
   /**Json name key missing*/
   DSErrorJsonNameKeyMissing               = -10034,
   /**The value of the key "Name" is duplicated.*/
   DSErrorJsonNameValueDuplicated          = -10035,
   /**Template name invalid*/
   DSErrorTemplateNameInvalid              = -10036,
   /**The name reference is invalid.*/
   DSErrorJsonNameReferenceInvalid         = -10037,
   /**Parameter value invalid*/
   DSErrorParameterValueInvalid            = -10038,
   /**The domain of your current site does not match the domain bound in the current product key.*/
   DSErrorDomainNotMatch                   = -10039,
   /**The license key does not match the license content.*/
   DSErrorLicenseKeyNotMatch               = -10043,
   /**Failed to set mode's argument.*/
   DSErrorSetModeArgumentError             = -10051,
   /**Failed to get mode's argument.*/
   DSErrorGetModeArgumentError             = -10055,
   /**The Intermediate Result Types license is invalid.*/
   DSErrorIrtLicenseInvalid                = -10056,
   /**Failed to save file.*/
   DSErrorFileSaveFailed                   = -10058,
   /**The stage type is invalid.*/
   DSErrorStageTypeInvalid                 = -10059,
   /**The image orientation is invalid.*/
   DSErrorImageOrientationInvalid          = -10060,
   /**Failed to convert complex tempalte to simplified settings.*/
   DSErrorConvertComplexTemplateError      = -10061,
   /**Reject function call while capturing in progress.*/
   DSErrorCallRejectedWhenCapturing        = -10062,
   /**The input image source was not found.*/
   DSErrorNoImageSource                    = -10063,
   /**Failed to read directory.*/
   DSErrorReadDirectoryFailed              = -10064,
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   DSErrorModuleNotFound                   = -10065,
   /**The file already exists but overwriting is disabled.*/
   DSErrorFileAlreadyExists                = -10067,
   /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
   DSErrorCreateFileFailed                 = -10068,
   /**The input ImageData object contains invalid parameter(s).*/
   DSErrorImageDataInvalid                 = -10069,
   /**The size of the input image does not meet the requirements.*/
   DSErrorImageSizeNotMatch                = -10070,
   /**The pixel format of the input image does not meet the requirements.*/
   DSErrorImagePixelFormatNotMatch         = -10071,
   /**The section level result is irreplaceable.*/
   DSErrorSectionLevelResultIrreplaceable  = -10072,
   /**The axis definition is incorrect.*/
   DSErrorAxisDefinitionIncorrect          = -10073,
   /**The result is not replaceable due to type mismatch*/
   DSErrorResultTypeMismatchIrreplaceable  = -10074,
   /**Failed to load the PDF library.*/
   DSErrorPDFLibraryLoadFailed             = -10075,
   /*The license is initialized successfully but detected invalid content in your key.*/
   DSErrorLicenseWarning                   = -10076,
   /*One or more unsupported JSON keys were encountered and ignored from the template.*/
   DSErrorUnsupportedJsonKeyWarning        = -10077,
   /**Model file is not found*/
   DSErrorModelFileNotFount                = -10078,
   /**[PDF] No license found.*/
   DSErrorPDFLicenseNotFound               = -10079,
   /**The rectangle is invalid.*/
   DSErrorRectInvalid                      = -10080,
   /*The template version is incompatible. Please use a compatible template.*/
   DSErrorTemplateVersionIncompatible      = -10081,
   /**No license.*/
   DSErrorNoLicense                        = -20000,
   /**Failed to read or write license cache. */
   DSErrorLicenseBufferFailed              = -20002,
   /**Falied to synchronize license info wirh license tracking server. */
   DSErrorLicenseSyncFailed                = -20003,
   /**Device does not match with license buffer. */
   DSErrorDeviceNotMatch                   = -20004,
   /**Falied to bind device. */
   DSErrorBindDeviceFailed                 = -20005,
   /**Install.*/
   DSErrorInstanceCountOverLimit           = -20008,
   /**Trial License*/
   DSErrorTrialLicense                     = -20010,
   /*License authentication failed: quota exceeded.*/
   DSErrorLicenseAuthQuotaExceeded         = -20013,
   /**License restriction: the number of results has exceeded the allowed limit.*/
   DSErrorLicenseResultsLimitExceeded      = -20014,
   /**The license is not valid for current version*/
   DSErrorLicenseVersionNotMatch           = -20011,
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   DSErrorBarcodeFormatInvalid             = -30009,
   /** The QR Code license is invalid. */
   DSErrorQRLicenseInvalid                 = -30016,
   /** The 1D Barcode license is invalid. */
   DSError1DLicenseInvalid                 = -30017,
   /** The PDF417 license is invalid. */
   DSErrorPDF417LicenseInvalid             = -30019,
   /** The DATAMATRIX license is invalid. */
   DSErrorDATAMATRIXLicenseInvalid         = -30020,
   /** The custom module size is invalid. */
   DSErrorCustomModuleSizeInvalid          = -30025,
   /** The AZTEC license is invalid. */
   DSErrorAztecLicenseInvalid              = -30041,
   /** The Patchcode license is invalid. */
   DSErrorPatchCodeLicenseInvalid          = -30046,
   /** The Postal code license is invalid. */
   DSErrorPostalCodeLicenseInvalid         = -30047,
   /** The DPM license is invalid. */
   DSErrorDPMLicenseInvalid                = -30048,
   /** The Maxicode license is invalid. */
   DSErrorMaxiCodeLicenseInvalid           = -30057,
   /** The GS1 Databar license is invalid. */
   DSErrorGS1DatabarLicenseInvalid         = -30058,
   /** The GS1 Composite code license is invalid. */
   DSErrorGS1CompositeLicenseInvalid       = -30059,
   /** The DotCode license is invalid. */
   DSErrorDotCodeLicenseInvalid            = -30061,
   /** The Pharmacode license is invalid. */
   DSErrorPharmaCodeLicenseInvalid         = -30062,
   /*[Barcode Reader] No license found.*/
   DSErrorDBRLicenseNotFound               = -30063,
   /** -40000~-49999: DLR error code */
   /** There is a conflict in the layout of TextLineGroup. */
   DSErrorTextLineGroupLayoutConflict      = -40101,
   /** There is a conflict in the regex of TextLineGroup. */
   DSErrorTextLineGroupRegexConflict       = -40102,
   /*[Label Recognizer] No license found.*/
   DSErrorDLRLicenseNotFound               = -40103,
   /** -50000~-59999: DDN error code. */
   /**No content has been detected. */
   DSErrorContentNotFound                  = -50056,
   /*The quardrilateral is invalid. */
   DSErrorQuadrilateralInvalid            = -50057,
   /*[Document Normalizer] No license found.*/
   DSErrorDDNLicenseNotFound               = -50058,
   /** -60000~-69999: DCE error code. */
   /** The camera module is not exist. */
   DSErrorCameraModelNotExist              = -60003,
   /** The camera id does not exist. */
   DSErrorCameraIDNotExist                 = -60006,
   /** The sensor does not exist. */
   DSErrorNoSensor                         = -60045,
   /** The camera type is not supported.*/
   DSErrorCameraTypeNotSupported           = -60046;
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   DSErrorPanoramaLicenseInvalid           = -70060,
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   DSErrorResourcePathNotExist             = -90001,
   /** Failed to load resource. */
   DSErrorResourceLoadFailed               = -90002,
   /** The code specification is not found. */
   DSErrorSpecificationNotFound        = -90003,
   /** The full code string is empty. */
   DSErrorFullCodeEmpty                    = -90004,
   /** Failed to preprocess the full code string */
   DSErrorFullCodePreprocessFailed         = -90005,
   /** The license for parsing South Africa Driver License is invalid. */
   DSErrorZADLLicenseInvalid               = -90006,
   /** The license for parsing North America DL/ID is invalid. */
   DSErrorAAMVADLIDLicenseInvalid          = -90007,
   /** The license for parsing Aadhaar is invalid. */
   DSErrorAADHAARLicenseInvalid            = -90008,
   /** The license for parsing Machine Readable Travel Documents is invalid. */
   DSErrorMRTDLicenseInvalid               = -90009,
   /** The license for parsing Vehicle Identification Number is invalid. */
   DSErrorVINLicenseInvalid                = -90010,
   /** The license for parsing customized code type is invalid. */
   DSErrorCustomizedCodeTypeLicenseInvalid = -90011,
   /*[Code Parser] No license found.*/
   DSErrorDCPLicenseNotFound               = -90012
};
```
>
```swift
public enum ErrorCode : Int
{
   /**Successful. */
   case ok                               = 0
   /**Unknown error. */
   case unknown                          = -10000
   /**Not enough memory to perform the operation. */
   case noMemory                         = -10001
   /**Null pointer */
   case nullPointer                      = -10002
   /**License invalid*/
   case licenseInvalid                   = -10003
   /**License expired*/
   case licenseExpired                   = -10004
   /**File not found*/
   case fileNotFound                     = -10005
   /**The file type is not supported. */
   case filetypeNotSupported             = -10006
   /**The BPP (Bits Per Pixel) is not supported. */
   case bppNotSupported                  = -10007
   /**Failed to read the image. */
   case imageReadFailed                  = -10012
   /**Failed to read the TIFF image. */
   case tiffReadFailed                   = -10013
   /**The DIB (Device-Independent Bitmaps) buffer is invalid. */
   case dibBufferInvalid                     = -10018,
   /**Failed to read the PDF image. */
   case pdfReadFailed                    = -10021
   /**The PDF DLL is missing. */
   case pdfDllMissing                    = -10022
   /**The page number is invalid. */
   case pageNumberInvalid                = -10023
   /**The custom size is invalid. */
   case customSizeInvalid                = -10024
   /** timeout. */
   case timeout                          = -10026
   /**Json parse failed*/
   case jsonParseFailed                  = -10030
   /**Json type invalid*/
   case jsonTypeInvalid                  = -10031
   /**Json key invalid*/
   case jsonKeyInvalid                   = -10032
   /**Json value invalid*/
   case jsonValueInvalid                 = -10033
   /**Json name key missing*/
   case jsonNameKeyMissing               = -10034
   /**The value of the key "Name" is duplicated.*/
   case jsonNameValueDuplicated          = -10035
   /**Template name invalid*/
   case templateNameInvalid              = -10036
   /**The name reference is invalid.*/
   case jsonNameReferenceInvalid         = -10037
   /**Parameter value invalid*/
   case parameterValueInvalid            = -10038
   /**The domain of your current site does not match the domain bound in the current product key.*/
   case domainNotMatch                   = -10039
   /**The license key does not match the license content.*/
   case licenseKeyNotMatch               = -10043
   /**Failed to set mode's argument.*/
   case setModeArgumentError             = -10051
   /**Failed to get mode's argument.*/
   case getModeArgumentError             = -10055
   /**The Intermediate Result Types license is invalid.*/
   case irtLicenseInvalid                = -10056
   /**Failed to save file.*/
   case fileSaveFailed                   = -10058
   /**The stage type is invalid.*/
   case stageTypeInvalid                 = -10059
   /**The image orientation is invalid.*/
   case imageOrientationInvalid          = -10060
   /**Failed to convert complex tempalte to simplified settings.*/
   case convertComplexTemplateError      = -10061
   /**Reject function call while capturing in progress.*/
   case callRejectedWhenCapturing        = -10062
   /**The input image source was not found.*/
   case noImageSource                    = -10063
   /**Failed to read directory.*/
   case readDirectoryFailed              = -10064
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   case moduleNotFound                   = -10065
   /**The file already exists but overwriting is disabled.*/
   case fileAlreadyExists                = -10067
   /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
   case createFileFailed                 = -10068
   /**The input ImageData object contains invalid parameter(s).*/
   case imageDataInvalid                 = -10069
   /**The size of the input image does not meet the requirements.*/
   case imageSizeNotMatch                = -10070
   /**The pixel format of the input image does not meet the requirements.*/
   case imagePixelFormatNotMatch         = -10071
   /**The section level result is irreplaceable.*/
   case sectionLevelResultIrreplaceable  = -10072
   /**The axis definition is incorrect.*/
   case axisDefinitionIncorrect          = -10073
   /**The result is not replaceable due to type mismatch*/
   case resultTypeMismatchIrreplaceable  = -10074
   /**Failed to load the PDF library.*/
   case pdfLibraryLoadFailed             = -10075
   /*The license is initialized successfully but detected invalid content in your key.*/
   case licenseWarning                   = -10076
   /*One or more unsupported JSON keys were encountered and ignored from the template.*/
   case unsupportedJsonKeyWarning        = -10077,
   /**Model file is not found*/
   case modelFileNotFount                = -10078,
   /**[PDF] No license found.*/
   case pdfLicenseNotFound               = -10079,
   /**The rectangle is invalid.*/
   case rectInvalid                      = -10080,
   /**No license.*/
   case noLicense                        = -20000
   /**Failed to read or write license cache. */
   case licenseBufferFailed              = -20002
   /**Falied to synchronize license info wirh license tracking server. */
   case licenseSyncFailed                = -20003
   /**Device does not match with license buffer. */
   case deviceNotMatch                   = -20004
   /**Falied to bind device. */
   case bindDeviceFailed                 = -20005
   /**Install.*/
   case instanceCountOverLimit           = -20008
   /**Trial License*/
   case trialLicense                     = -20010
   /**The license is not valid for current version*/
   case licenseVersionNotMatch           = -20011
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   case barcodeFormatInvalid             = -30009
   /** The custom module size is invalid. */
   case customModuleSizeInvalid          = -30025
   /*[Barcode Reader] No license found.*/
   case dbrLicenseNotFound               = -30063
   /** -40000~-49999: DLR error code */
   /** There is a conflict in the layout of TextLineGroup. */
   case textLineGroupLayoutConflict      = -40101
   /** There is a conflict in the regex of TextLineGroup. */
   case textLineGroupRegexConflict       = -40102
   /*[Label Recognizer] No license found.*/
   case dlrLicenseNotFound               = -40103
   /** -50000~-59999: DDN error code. */
   /** No content has been detected. */
   case contentNotFound                  = -50056
   /*The quardrilateral is invalid. */
   case quardrilateralInvalid            = -50057
   /*[Document Normalizer] No license found.*/
   case ddnLicenseNotFound               = -50058
   /** -60000~-69999: DCE error code. */
   /** The camera module is not exist. */
   case cameraModelNotExist              = -60003
   /** The camera id does not exist. */
   case cameraIDNotExist                 = -60006
   /** The sensor does not exist. */
   case noSensor                         = -60045
   /** The camera type is not supported.*/
   case cameraTypeNotSupported           = -60046;
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   case panoramaLicenseInvalid           = -70060
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   case resourcePathNotExist             = -90001
   /** Failed to load resource. */
   case resourceLoadFailed               = -90002
   /** The code specification is not found. */
   case codeSpecificationNotFound        = -90003
   /** The full code string is empty. */
   case fullCodeEmpty                    = -90004
   /** Failed to preprocess the full code string */
   case fullCodePreprocessFailed         = -90005
   /*[Code Parser] No license found.*/
   case dcpLicenseNotFound               = -90012
}
```
