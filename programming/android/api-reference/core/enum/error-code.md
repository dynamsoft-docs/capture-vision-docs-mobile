---
layout: default-layout
title: ErrorCode - Dynamsoft Capture Vision Android Enumerations
description: The enumeration ErrorCode of Dynamsoft Capture Vision Android describes all error codes.
keywords: Error code
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ErrorCode
codeAutoHeight: true
---

# Enumeration ErrorCode

`ErrorCode` enumerates the specific error codes that the SDK may return, providing a systematic way to identify and handle errors encountered during its operation.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumErrorCode
{
   /** Successful. */
   int EC_OK = 0;
   /** -10000~-19999: Common error code. */
   /** Unknown error. */
   int EC_UNKNOWN = -10000,
   /**Not enough memory to perform the operation. */
   int EC_NO_MEMORY = -10001,
   /** Null pointer */
   int EC_NULL_POINTER = -10002,
   /** License invalid. */
   int EC_LICENSE_INVALID = -10003,
   /** License expired. */
   int EC_LICENSE_EXPIRED = -10004,
   /** File not found. */
   int EC_FILE_NOT_FOUND = -10005,
   /** The file type is not supported. */
   int EC_FILE_TYPE_NOT_SUPPORTED = -10006,
   /** The BPP (Bits Per Pixel) is not supported. */
   int EC_BPP_NOT_SUPPORTED = -10007,
   /** The index is invalid. */
   int EC_INDEX_INVALID = -10008,
   /** The input region value parameter is invalid. */
   int EC_CUSTOM_REGION_INVALID = -10010,
   /** Failed to read the image. */
   int EC_IMAGE_READ_FAILED = -10012,
   /** Failed to read the TIFF image. */
   int EC_TIFF_READ_FAILED = -10013,
   /** The DIB (Device-Independent Bitmaps) buffer is invalid. */
   int EC_DIB_BUFFER_INVALID = -10018,
   /** Failed to read the PDF image. */
   int EC_PDF_READ_FAILED = -10021,
   /** The PDF DLL is missing. */
   int EC_PDF_DLL_MISSING = -10022,
   /** The page number is invalid. */
   int EC_PAGE_NUMBER_INVALID = -10023,
   /** The custom size is invalid. */
   int EC_CUSTOM_SIZE_INVALID = -10024,
   /** timeout. */
   int EC_TIMEOUT = -10026,
   /** Json parse failed. */
   int EC_JSON_PARSE_FAILED = -10030,
   /** Json type invalid. */
   int EC_JSON_TYPE_INVALID = -10031,
   /** Json key invalid. */
   int EC_JSON_KEY_INVALID = -10032,
   /** Json value invalid. */
   int EC_JSON_VALUE_INVALID = -10033,
   /** Json name key missing. */
   int EC_JSON_NAME_KEY_MISSING = -10034,
   /** The value of the key "Name" is duplicated. */
   int EC_JSON_NAME_VALUE_DUPLICATED = -10035,
   /** Template name invalid. */
   int EC_TEMPLATE_NAME_INVALID = -10036,
   /** The name reference is invalid. */
   int EC_JSON_NAME_REFERENCE_INVALID = -10037,
   /** Parameter value invalid. */
   int EC_PARAMETER_VALUE_INVALID = -10038,
   /** The domain of your current site does not match the domain bound in the current product key. */
   int EC_DOMAIN_NOT_MATCH = -10039,
   /** The reserved info does not match the reserved info bound in the current product key. */
   int EC_RESERVED_INFO_NOT_MATCH = -10040,
   /** The license key does not match the license content. */
   int EC_LICENSE_KEY_NOT_MATCH = -10043,
   /** Failed to request the license content. */
   int EC_REQUEST_FAILED = -10044,
   /** Failed to init the license. */
   int EC_LICENSE_INIT_FAILED = -10045,
   /** Failed to set mode's argument. */
   int EC_SET_MODE_ARGUMENT_ERROR = -10051,
   /** The license content is invalid. */
   int EC_LICENSE_CONTENT_INVALID = -10052,
   /** The license key is invalid. */
   int EC_LICENSE_KEY_INVALID = -10053,
   /** The license key has no remaining quota. */
   int EC_LICENSE_DEVICE_RUNS_OUT = -10054,
   /** Failed to get mode's argument. */
   int EC_GET_MODE_ARGUMENT_ERROR = -10055,
   /** The Intermediate Result Types license is invalid. */
   int EC_IRT_LICENSE_INVALID = -10056,
   /** Failed to save file. */
   int EC_FILE_SAVE_FAILED = -10058,
   /** The stage type is invalid. */
   int EC_STAGE_TYPE_INVALID = -10059,
   /** The image orientation is invalid. */
   int EC_IMAGE_ORIENTATION_INVALID = -10060,
   /** Complex tempalte can't be converted to simplified settings. */
   int EC_CONVERT_COMPLEX_TEMPLATE_ERROR = -10061,
   /** Reject function call while capturing in progress.*/
   int EC_CALL_REJECTED_WHEN_CAPTURING = -10062,
   /**The input image source was not found.*/
   int EC_NO_IMAGE_SOURCE = -10063,
   /**Failed to read directory.*/
   int EC_READ_DIRECTORY_FAILED = -10064,
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   int EC_MODULE_NOT_FOUND = -10065,
   /**The file already exists but overwriting is disabled.*/
   int EC_FILE_ALREADY_EXISTS = -10067,
   /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
   int EC_CREATE_FILE_FAILED = -10068,
   /**The input ImageData object contains invalid parameter(s).*/
   int EC_IMGAE_DATA_INVALID = -10069,
   /**The size of the input image do not meet the requirements.*/
   int EC_IMAGE_SIZE_NOT_MATCH = -10070,
   /**The pixel format of the input image do not meet the requirements.*/
   int EC_IMAGE_PIXEL_FORMAT_NOT_MATCH = -10071,
   /**The section level result is irreplaceable.*/
   int EC_SECTION_LEVEL_RESULT_IRREPLACEABLE = -10072,
   /**The axis definition is incorrect.*/
   int EC_AXIS_DEFINITION_INCORRECT = -10073,
   /**The result is not replaceable due to type mismatch*/
   int EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE = -10074,
   /**Failed to load the PDF library.*/
   int EC_PDF_LIBRARY_LOAD_FAILED = -10075,
   /*The license is initialized successfully but detected invalid content in your key.*/
   int EC_LICENSE_WARNING = -10076,
   /*The template version is incompatible. Please use a compatible template.*/
   int EC_TEMPLATE_VERSION_INCOMPATIBLE = -10081
   /** -20000~-29999: DLS license error code. */
   /** No license. */
   int EC_NO_LICENSE = -20000,
   /** The Handshake Code is invalid. */
   int EC_HANDSHAKE_CODE_INVALID = -20001,
   /** Failed to read or write license buffer. */
   int EC_LICENSE_BUFFER_FAILED = -20002,
   /** Failed to synchronize license info with license server. */
   int EC_LICENSE_SYNC_FAILED = -20003,
   /** Device dose not match with buffer. */
   int EC_DEVICE_NOT_MATCH = -20004,
   /** Failed to bind device. */
   int EC_BIND_DEVICE_FAILED = -20005,
   /** Instance count is over limit. */
   int EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
   /** Trial License */
   int EC_TRIAL_LICENSE = -20010,
   /*License authentication failed: quota exceeded.*/
   int EC_LICENSE_AUTH_QUOTA_EXCEEDED = -20013,
   /**License restriction: the number of results has exceeded the allowed limit.*/
   int EC_LICENSE_RESULTS_LIMIT_EXCEEDED = -20014,
   /** Failed to reach License Server. */
   int EC_FAILED_TO_REACH_DLS = -20200,
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   int EC_BARCODE_FORMAT_INVALID = -30009,
   /** The QR Code license is invalid. */
   int EC_QR_LICENSE_INVALID = -30016,
   /** The 1D Barcode license is invalid. */
   int EC_1D_LICENSE_INVALID = -30017,
   /** The PDF417 license is invalid. */
   int EC_PDF417_LICENSE_INVALID = -30019,
   /** The DATAMATRIX license is invalid. */
   int EC_DATAMATRIX_LICENSE_INVALID = -30020,
   /** The custom module size is invalid. */
   int EC_CUSTOM_MODULESIZE_INVALID = -30025,
   /** The AZTEC license is invalid. */
   int EC_AZTEC_LICENSE_INVALID = -30041,
   /** The Patchcode license is invalid. */
   int EC_PATCHCODE_LICENSE_INVALID = -30046,
   /** The Postal code license is invalid. */
   int EC_POSTALCODE_LICENSE_INVALID = -30047,
   /** The DPM license is invalid. */
   int EC_DPM_LICENSE_INVALID = -30048,
   /** The frame decoding thread already exists. */
   int EC_FRAME_DECODING_THREAD_EXISTS = -30049,
   /** Failed to stop the frame decoding thread. */
   int EC_STOP_DECODING_THREAD_FAILED = -30050,
   /** The Maxicode license is invalid. */
   int EC_MAXICODE_LICENSE_INVALID = -30057,
   /** The GS1 Databar license is invalid. */
   int EC_GS1_DATABAR_LICENSE_INVALID = -30058,
   /** The GS1 Composite code license is invalid. */
   int EC_GS1_COMPOSITE_LICENSE_INVALID = -30059,
   /** The DotCode license is invalid. */
   int EC_DOTCODE_LICENSE_INVALID = -30061,
   /** The Pharmacode license is invalid. */
   int EC_PHARMACODE_LICENSE_INVALID = -30062,
   /*[Barcode Reader] No license found.*/
   int EC_DBR_LICENSE_NOT_FOUND = -30063,
   /** -40000~-49999: DLR error code */
   /** Character Model file is not found. */
   int EC_CHARACTER_MODEL_FILE_NOT_FOUND = -40100,
   /**There is a conflict in the layout of TextLineGroup. */
   int EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT = -40101,
   /**There is a conflict in the regex of TextLineGroup. */
   int EC_TEXT_LINE_GROUP_REGEX_CONFLICT = -40102,
   /*[Label Recognizer] No license found.*/
   int EC_DLR_LICENSE_NOT_FOUND = -40103,
   /** -50000~-59999: DDN error code. */
   /**No content has been detected. */
   int EC_CONTENT_NOT_FOUND = -50056,
   /*The quardrilateral is invalid. */
   int EC_QUADRILATERAL_INVALID = -50057,
   /*[Document Normalizer] No license found.*/
   int EC_DDN_LICENSE_NOT_FOUND = -50058,
   /** -60000~-69999: DCE error code. */
   /**-60000~-69999: DCE error code*/
   /** The camera module is not exist. */
   int EC_CAMERA_MODULE_NOT_EXIST = -60003;
   /** The camera id does not exist. */
   int EC_CAMERA_ID_NOT_EXIST = -60006;
   /** The sensor does not exist. */
   int EC_NO_SENSOR = -60045;
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   int EC_PANORAMA_LICENSE_INVALID = -70060,
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   int EC_RESOURCE_PATH_NOT_EXIST = -90001,
   /** Failed to load resource. */
   int EC_RESOURCE_LOAD_FAILED = -90002,
   /** The code specification is not found. */
   int EC_CODE_SPECIFICATION_NOT_FOUND = -90003,
   /** The full code string is empty. */
   int EC_FULL_CODE_EMPTY = -90004,
   /** Failed to preprocess the full code string */
   int EC_FULL_CODE_PREPROCESS_FAILED = -90005,
   /** The license for parsing South Africa Driver License is invalid. */
   int EC_ZA_DL_LICENSE_INVALID = -90006,
   /** The license for parsing North America DL/ID is invalid. */
   int EC_AAMVA_DL_ID_LICENSE_INVALID = -90007,
   /** The license for parsing Aadhaar is invalid. */
   int EC_AADHAAR_LICENSE_INVALID = -90008,
   /** The license for parsing Machine Readable Travel Documents is invalid. */
   int EC_MRTD_LICENSE_INVALID = -90009,
   /** The license for parsing Vehicle Identification Number is invalid. */
   int EC_VIN_LICENSE_INVALID = -90010,
   /** The license for parsing customized code type is invalid. */
   int EC_CUSTOMIZED_CODE_TYPE_LICENSE_INVALID = -90011,
   /*[Code Parser] No license found.*/
   int EC_DCP_LICENSE_NOT_FOUND = -90012
} ErrorCode;
```
