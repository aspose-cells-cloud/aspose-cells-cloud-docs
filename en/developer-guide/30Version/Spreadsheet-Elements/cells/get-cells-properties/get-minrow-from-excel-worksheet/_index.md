---
title: "Get MinRow from Excel Worksheet – Aspose.Cells Cloud API Reference"
type: docs
url: /get-minrow-from-excel-worksheet/
weight: 80
date: 2023-11-15
description: "Get first non-empty row index in Excel worksheet via Aspose.Cells Cloud REST API v3.0 with cURL and SDK examples"
keywords: "Aspose.Cells, GetMinRow, Excel worksheet, REST API, min row index, cloud SDK"
ArticleTitle: "Get MinRow from Excel Worksheet – Aspose.Cells Cloud API Reference"
linktitle: "Get MinRow"
---
The **GetWorksheetCell** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}`) enables retrieval of cell data or special method-based values—such as the minimum row index—directly from an Excel worksheet in Aspose.Cells Cloud, allowing developers to programmatically determine properties like the first non-empty row (zero-based) by passing `minrow` as the `cellOrMethodName` parameter.

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

- **cURL Example:**

{{< tabs tabTotal="9" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

> _“Replace `<access_token>` with a valid OAuth 2.0 access token. Generate one via the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).”_

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**Request**


| Property          | Type   | Required | Description                                            |
|-------------------|--------|----------|--------------------------------------------------------|
| `fileName`        | string | Yes      | Name of the workbook (e.g., `myWorkbook.xlsx`).        |
| `sheetName`       | string | Yes      | Target worksheet (e.g., `Sheet1`).                     |
| `cellOrMethodName`| string | Yes      | Fixed value `minrow`.                                   |
| `folder`          | string | No       | Cloud storage folder path.                             |
| `storageName`     | string | No       | Storage name if a non‑default storage is used.        |

**Response**

The service returns a JSON object that contains the `MinRow` property, indicating the index of the first non‑empty row (zero‑based).

| HTTP Status | Meaning                                 |
|-------------|------------------------------------------|
| 200         | Success – JSON payload with `MinRow`.   |
| 401         | Unauthorized – invalid or missing token.|
| 404         | Workbook or worksheet not found.        |
| 500         | Internal server error.                  |

The `MinRow` value is useful when you need to quickly locate the starting point of data in a sheet.

- **Use Aspose.Cells Cloud SDKs**

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}

> _**Note:** This endpoint uses Aspose.Cells Cloud API v3.0. We recommend migrating to [v4.0](/v4-apis) for improved performance and features._

> _Related APIs: [Get MaxRow](/get-maxrow-from-excel-worksheet/), [Get Cell](/get-cell-from-excel-worksheet/). For SDK setup guidance, see [Set Up SDKs](/setup-sdk/)._