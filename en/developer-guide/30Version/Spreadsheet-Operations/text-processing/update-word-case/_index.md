---
title: "Aspose.Cells – Update Word Case API"
second_title: "Developer Guide"
linktitle: "Word Case"
type: docs
url: /post-update-word-case/
keywords: "Aspose.Cells, Update Word Case API, text case conversion, Excel, CSV, Google Sheets, REST API"
description: "PostUpdateWordCase API converts text case in Excel, CSV, Google Sheets via REST: Upper, Lower, Capitalize, Title case."
weight: 100
ArticleTitle: "Aspose.Cells – Update Word Case API Documentation"
---

The **PostUpdateWordCase** API (`POST https://api.aspose.cloud/v3.0/cells/updatewordcase`) in Aspose.Cells Cloud automates text-case conversions to address the common issue of inconsistent text case in spreadsheets, which can significantly impact data analysis and processing, and works with a wide range of formats including Excel, Google Sheets, OpenOffice, JSON, CSV, and others, applying rules such as uppercase-to-lowercase, lowercase-to-uppercase, capitalize-first-letter, and title case (where the first letter of each major word is capitalized) to specified text ranges, so that large datasets can be cleaned, standardized, and made ready for further manipulation or analysis with minimal effort.

## The Post Update Word Case Web API

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name  | Type                  | Path/Query String/HTTPBody | Description |
| --------------- | --------------------- | -------------------------- | ----------- |
| wordCaseOptions | class:wordcaseoptions | HTTPBody                   | -           |

**`wordCaseOptions` schema**

```json
{
  "Range": "A1:B10", // Excel‑style range to process (required)
  "CaseType": "Upper", // Enum: Upper, Lower, Capitalize, Title (required)
  "IgnoreBlank": true // Boolean, optional – when true, blank cells are left unchanged
}
```

**Example request body**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – The cell range to which the case conversion will be applied (e.g., `A1:C5`).
- **CaseType** – The type of case conversion. Allowed values are `Upper`, `Lower`, `Capitalize`, and `Title`.
- **IgnoreBlank** – If `true`, blank cells are ignored; default is `false`.

### Response

```json
[
  {
    "Name": "FileInfo",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FileInfo"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

- **Filename** – Name of the processed file.
- **FileSize** – Size of the file in bytes.
- **FileContent** – Base‑64 encoded content of the transformed file.

## How to Use the Post Update Word Case API with SDKs?

### Post Update Word Case API Specification

The <a href="https://reference.aspose.cloud/cells/#/TextProcessing/PostUpdateWordCase" rel="noopener noreferrer">Post Update Word Case API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
