---
title: "Save Options"
second_title: "Document"
linktitle: "Save options"
type: docs
url: /save-options/
date: 2024-03-15T10:00:00Z
lastmod: 2024-05-22T14:30:00Z
keywords: "Aspose.Cells Cloud, SaveOptions, REST API, Excel save, PDF export, HTTP compression"
description: "Configure workbook saving behavior in Aspose.Cells Cloud REST API using SaveOptions — including HTTP compression, chart refresh, and directory creation. Full parameter reference with examples."
weight: 79
ArticleTitle: "Save Options – Aspose.Cells Cloud REST API Documentation"
---

# SaveOptions Properties

SaveOptions allow you to control how a workbook is saved when using the Aspose.Cells Cloud REST API. By configuring these options you can enable HTTP compression, specify the output format, manage temporary storage, and control additional behaviors such as chart cache refresh and automatic directory creation.

**Prerequisites**  
- An authenticated Aspose.Cells Cloud session ([OAuth 2.0 setup](/oauth-setup)).  
- The target workbook must be loaded or created via the API prior to saving ([Create or load workbook via API](/workbook-operations)).

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

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

**Notes / Remarks**  
- When **CreateDirectory** is set to `true`, the API will automatically create the target folder if it does not already exist.  
- Enabling **EnableHTTPCompression** can reduce payload size for large workbooks, but the client must support gzip/deflate decoding ([RFC 7694](https://datatracker.ietf.org/doc/html/rfc7694)).  
- **RefreshChartCache** should be used when charts rely on dynamic data that may have changed since the workbook was generated. For more information, see [Learn more about file formats](/supported-formats).