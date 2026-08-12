---
title: "Merge Matching Spreadsheets in Remote Folder"
description: "Combine spreadsheet files stored in Aspose Cloud storage into a single file. Supports 30+ output formats such as PDF, CSV, JSON, XLSX, ODS, XPS, and more."
keywords: "Aspose.Cells, merge spreadsheets, remote folder, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

Combine multiple spreadsheet files that reside in a remote Aspose Cloud storage folder into a single output file. The operation runs entirely in the cloud, eliminating the need to download source files locally. Over 30 output formats are supported (PDF, CSV, JSON, XLSX, ODS, XPS, …).

## MergeSpreadsheetsInRemoteFolder API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters <a id="request-parameters"></a>

| Name                    | Type    | Location | Required | Description                                                                                          |
| ----------------------- | ------- | -------- | -------- | ---------------------------------------------------------------------------------------------------- |
| **folder**              | string  | query    | **Yes**  | Cloud storage folder that contains the source spreadsheets.                                          |
| **fileMatchExpression** | string  | query    | **Yes**  | Pattern to select files (e.g., `*report*.xlsx`). Supports wildcards `*` and `?`.                     |
| **outFormat**           | string  | query    | **Yes**  | Desired output format (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …).                               |
| **mergeInOneSheet**     | boolean | query    | **Yes**  | `true` – all data merged into a single worksheet. `false` – each source file gets its own worksheet. |
| **storageName**         | string  | query    | No       | Custom storage name; defaults to the primary storage if omitted.                                     |
| **outPath**             | string  | query    | No       | Destination folder for the merged file. If omitted, the file is saved in the source folder.          |
| **outStorageName**      | string  | query    | No       | Storage name where the merged file will be written.                                                  |
| **fontsLocation**       | string  | query    | No       | Path to a folder containing custom fonts (required for PDF/Image export).                            |
| **region**              | string  | query    | No       | Locale for number, date, and currency formatting (e.g., `en-US`, `de-DE`).                           |
| **password**            | string  | query    | No       | Password to open any protected source spreadsheet.                                                   |

## Request Example (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **Response**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

The file can be downloaded directly from the `FileUrl` or saved to the location specified by `outPath`.

**Success response details**

| Status Code  | Content‑Type               | Description                                 |
| ------------ | -------------------------- | ------------------------------------------- |
| 200 OK       | `application/octet-stream` | Binary stream of the merged workbook file.  |
| 202 Accepted | `application/json`         | JSON containing `FileUrl`, `FileName`, etc. |

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## How to Use the Merge Spreadsheet API with SDKs

### OpenAPI Specification

The <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI Specification</a> provides a machine‑readable description of the API, enabling direct REST interactions.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to import data into a spreadsheet worksheet with short code. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
