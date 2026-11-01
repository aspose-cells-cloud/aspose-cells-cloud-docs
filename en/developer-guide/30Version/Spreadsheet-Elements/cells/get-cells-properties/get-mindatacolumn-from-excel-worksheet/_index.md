---
title: "Get MinDataColumn – Aspose.Cells Cloud API Reference (v3.0)"
date: 2023-11-15
lastmod: 2024-05-22
type: docs
url: /get-mindatacolumn-from-excel-worksheet/
weight: 110
description: "Retrieve the zero-based index of the leftmost data column in an Excel worksheet via Aspose.Cells Cloud REST API v3.0."
ArticleTitle: "Get MinDataColumn – Aspose.Cells Cloud API Reference (v3.0)"
keywords: "mindatacolumn, leftmost data column, Excel API, REST API, Aspose.Cells, cloud spreadsheet, zero-based index, Aspose.Cells Cloud API v3.0"
linktitle: "Get MinDataColumn"
---
The **GetWorksheetCell** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}`) retrieves cell data from a specified Excel worksheet using either a standard cell reference (e.g., "A1") or a method name such as "mindatacolumn" to return the zero-based index of the leftmost column containing data. Aspose.Cells Cloud supports this operation to simplify programmatic access to structured worksheet content, enabling developers to efficiently determine data boundaries without manual iteration.

## The Get Worksheet Cell Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| cellOrMethodName | String | Path | The cell's or method name. (Method name like firstcell, endcell etc.) |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### **Response**

```json
[
  {
    "Name": "String",
    "DataType": {
      "Identifier": "String"
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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

> **Definition** – `mindatacolumn`: the index (starting at 0) of the first column that contains data in the worksheet.

**Prerequisites**  
- A valid OAuth2 access token is required.  
- The Excel file must be uploaded to Aspose Cloud storage.

### Request Parameters

| Parameter      | Type   | Required | Description                                 |
|----------------|--------|----------|---------------------------------------------|
| `fileName`     | string | Yes      | Name of the Excel file stored in cloud storage. |
| `sheetName`    | string | Yes      | Name of the worksheet from which to retrieve the column index. |
| `Authorization` (header) | string | Yes | Bearer token for OAuth2 authentication. |

- **cURL Example**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

### HTTP Status Codes

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Request successful; response contains the `MinDataColumn` (zero-based index). |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 403  | Forbidden                   | Invalid OAuth2 scope or insufficient permissions. |
| 404  | Not Found                   | File or worksheet not found. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

- Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to accelerate development. An SDK handles low‑level details, allowing you to focus on your project logic. Please check the [Aspose.Cells Cloud SDKs GitHub organization](https://github.com/aspose-cells-cloud), where each SDK repo includes versioned examples, changelogs, and issue templates.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}