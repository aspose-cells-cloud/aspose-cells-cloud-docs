---
title: "Save Options"
second_title: "Document"
linktitle: "Save options"
type: docs
url: /save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Workbook, REST API, File Formats, PDF, CSV, JSON, HTTP Compression, Chart Cache, Named Ranges, Directory Creation"
description: "Describes the SaveOptions properties of the Aspose.Cells Cloud REST API, enabling developers to configure workbook‑saving behavior across multiple file formats and options such as HTTP compression, chart cache refresh, and automatic directory creation."
weight: 79
ArticleTitle: "Save Options – Aspose.Cells Cloud REST API Documentation"
---

# SaveOptions Properties

SaveOptions allow you to control how a workbook is saved when using the Aspose.Cells Cloud REST API. By configuring these options you can enable HTTP compression, specify the output format, manage temporary storage, and control additional behaviors such as chart cache refresh and automatic directory creation.

**Prerequisites**  
- An authenticated Aspose.Cells Cloud session (OAuth 2.0 or JWT).  
- The target workbook must be loaded or created via the API prior to saving.

| Name                      | Type       | Description                                                                                        | Notes      |
| ------------------------- | ---------- | -------------------------------------------------------------------------------------------------- | ---------- |
| **EnableHTTPCompression** | **bool?**  | Enables HTTP compression for the response.                                                         | [optional] |
| **SaveFormat**            | **string** | Specifies the target file format for saving the workbook.                                          | [optional] |
| **ClearData**             | **bool?**  | Makes the workbook empty after saving the file.                                                    | [optional] |
| **CachedFileFolder**      | **string** | The cached file folder used to store large data temporarily.                                       | [optional] |
| **ValidateMergedAreas**   | **bool?**  | Indicates whether to validate merged areas before saving the file. The default value is false.     | [optional] |
| **RefreshChartCache**     | **bool?**  | Refreshes chart cache data before saving.                                                          | [optional] |
| **CreateDirectory**       | **bool?**  | If true and the directory does not exist, it will be automatically created before saving the file. | [optional] |
| **SortNames**             | **bool?**  | Sorts named ranges alphabetically when saving.                                                     | [optional] |

**Request**  
- **Method:** `POST` (or `PUT` depending on the operation)  
- **Endpoint:** `/cells/workbook/save`  
- **Headers:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **Body:** JSON representation of the `SaveOptions` model (the table above) combined with the workbook data or reference.

**Response Example**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "Workbook saved successfully."
}
```

**Status Codes**  

| Code | Meaning                                 |
|------|------------------------------------------|
| 200  | Save operation completed successfully.   |
| 400  | Invalid request – missing or malformed parameters. |
| 401  | Unauthorized – authentication failed.    |
| 500  | Server error – unexpected failure during processing. |

**Notes / Remarks**  
- When **CreateDirectory** is set to `true`, the API will automatically create the target folder if it does not already exist.  
- Enabling **EnableHTTPCompression** can reduce payload size for large workbooks, but the client must support gzip/deflate decoding.  
- **RefreshChartCache** should be used when charts rely on dynamic data that may have changed since the workbook was generated.

**See also**  
- Convert Workbook Options  
- AutoFitterOptions  
- Workbook API Overview  

---