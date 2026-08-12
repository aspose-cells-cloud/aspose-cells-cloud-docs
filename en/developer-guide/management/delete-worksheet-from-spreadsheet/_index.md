---
title: "Aspose.Cells Cloud Excel Delete Worksheet Web API - Remove Sheets from Workbooks Programmatically"
second_title: "Document"
ArticleTitle: "How to Delete Worksheets from Excel - Remove Sheets from Workbooks"
linktitle: "Delete Worksheet from Spreadsheet"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, delete worksheet API, Excel sheet removal, cloud spreadsheet, REST API"
description: "Learn how to delete a worksheet from an Excel file using Aspose.Cells Cloud API. Includes endpoint, parameters, sample cURL, and SDK examples."
weight: 100
---

Programmatically delete worksheets from Excel workbooks using Aspose.Cells Cloud API. Safely remove single or multiple sheets, clean up workbook structure, and automate spreadsheet optimization. RESTful API for enterprise‑grade Excel management and document‑processing workflows.

## Delete worksheet from Spreadsheet API

### Web API

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters:

| Parameter Name | Type   | Location | Description                                                                                                                                                                                             |
| :------------- | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | File   | FormData | **Required.** The source Excel workbook file (.xlsx, .xls, etc.) from which a worksheet will be removed.                                                                                                |
| sheetName      | String | Query    | **Required.** The exact name of the worksheet to be deleted (e.g., `Sheet1`, `TemporaryData`).                                                                                                          |
| outPath        | String | Query    | **Optional.** The target folder path in cloud storage where the modified workbook will be saved. If omitted or `null`, the workbook is saved in the same location as the source file or a default path. |
| outStorageName | String | Query    | **Optional.** The identifier of the cloud storage service (e.g., `ProjectStorage`) where the output file will be written. If not supplied, the default storage is used.                                 |
| region         | String | Query    | **Optional.** The locale setting (e.g., `it-IT`) that may affect region‑specific formulas or data during the save operation.                                                                            |
| password       | String | Query    | **Optional.** The password required to open and modify a password‑protected spreadsheet. Omit if the file is not encrypted.                                                                             |

### Response

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## Where should we use the Delete worksheet from Spreadsheet API?

- **Automated Report Post‑processing** – After generating a final financial report, automatically remove intermediate worksheets used for temporary calculations, keeping the final file clean and professional.
- **Dynamic Cleanup of Template Files** – When users generate customized documents (e.g., quotations) from a template, delete optional pages that were not selected.
- **Optimization of Workflow Archiving** – After a project or audit is completed, remove draft or collaboration worksheets, retaining only the final version for archiving and compliance.

## Why should you use the Delete worksheet from Spreadsheet API?

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development and providing comprehensive documentation.
- **Reduced Labor Costs** – Eliminates the need for dedicated personnel to consolidate documents manually.
- **Pay‑per‑Use** – No upfront investment; you only pay for the API calls you actually use.
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility concerns.

## How to Use the Delete worksheet from Spreadsheet API with SDKs

### Delete worksheet from Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">Delete worksheet from Spreadsheet API Specification</a> defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

Using an SDK is the fastest way to develop, as it abstracts low‑level details and lets you delete a worksheet with minimal code. Please check the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
