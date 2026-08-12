---
title: "Aspose.Cells Cloud Excel Unprotect Web API – Programmatically Remove Open & Modify Passwords"
second_title: "Document"
ArticleTitle: "Remove Excel Password Protection – Unlock Open & Modify Passwords Instantly"
linktitle: "Unprotect Spreadsheet"
type: docs
url: /unprotect-spreadsheet/
keywords: "unprotect, spreadsheet, Aspose.Cells, API, Excel, password removal"
description: "Remove open and modify passwords from Excel files programmatically with the Aspose.Cells Cloud Unprotect Spreadsheet API. Supports .xlsx/.xls, OAuth2 authentication, and batch processing."
weight: 100
---

The Unprotect Spreadsheet API removes open‑ and modify‑password protection from Excel files in a single call. It is ideal for data pipelines, document‑management systems, and migration workflows.

## **Unprotect Spreadsheet API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Request Parameters**

| Parameter Name | Type   | Location | Description                                                                          |
| -------------- | ------ | -------- | ------------------------------------------------------------------------------------ |
| Spreadsheet    | File   | FormData | The Excel file to be unprotected.                                                    |
| password       | String | Query    | The password that protects the file for opening.                                     |
| modifyPassword | String | Query    | The password required to modify the file (optional if only an open password is set). |
| outPath        | String | Query    | (Optional) Folder path where the unprotected workbook will be saved.                 |
| outStorageName | String | Query    | (Optional) Name of the storage where the output file will be written.                |
| region         | String | Query    | (Optional) Spreadsheet region settings.                                              |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

A successful response returns the unprotected file as a stream. The file can be saved to the location specified by `outPath`/`outStorageName` or retrieved directly from the response payload.

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## When should you use the Unprotect Spreadsheet API?

- **Restore Access to Locked Workbooks** – Quickly remove forgotten open or modify passwords without manual intervention.
- **Automate Bulk Unlocking** – Process large numbers of files in data‑migration or archival projects.
- **Integrate with Existing Workflows** – Combine with storage or conversion APIs to create end‑to‑end pipelines (e.g., upload → unprotect → convert to PDF).
- **Maintain Data Security** – The operation occurs on the server side, keeping the original files secure while the unprotected version is stored in your cloud storage.

## How to use the Unprotect Spreadsheet API with SDKs

### OpenAPI Specification

The [UnProtect Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) provides a publicly accessible programming interface to facilitate direct REST interactions from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

Using an SDK simplifies the call by handling authentication, request construction, and response parsing. The SDKs are available for many languages and include ready‑made methods for unprotecting spreadsheets.

The following code examples illustrate how to call the Unprotect Spreadsheet API using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
