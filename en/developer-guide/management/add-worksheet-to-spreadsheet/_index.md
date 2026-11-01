---
title: "Add Worksheet to Excel Workbook — Aspose.Cells Cloud API"
description: "Add Excel worksheet, chart, or macro sheet via Aspose.Cells Cloud API with type, name, and position control"
date: 2024-05-10
lastmod: 2024-06-15
draft: false
url: /add-worksheet-to-spreadsheet/
linktitle: "Add Worksheet to Spreadsheet"
type: docs
keywords: "add worksheet to excel, excel api, aspose.cells cloud, insert sheet, spreadsheet automation, chart sheet, macro sheet, REST API"
weight: 100
ArticleTitle: "Add Worksheet to Excel Workbook with Aspose.Cells Cloud REST API"
---
The **AddWorksheetToSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet`) enables users to add a new worksheet, chart sheet, or macro sheet to an Excel workbook via the Aspose.Cells Cloud REST API by specifying the worksheet type, insertion position, and name; it supports dynamic workbook structuring for automated reporting, template generation, and audit workflows, and accepts a spreadsheet file upload along with optional query parameters for fine-grained control.

## The Add Worksheet to Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| sheetType | String | Query | Specifies the name of the new worksheet.If not provided, a default name will be assigned. |
| position | Integer | Query | Specifies the position at which the new worksheet should be inserted.If not provided, the worksheet will be added at the end of the workbook. |
| sheetName | String | Query | Specifies the type of worksheet to be added.If not provided, a default worksheet type will be used. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

On success, the API returns **HTTP 200 OK** with the updated workbook in the response body.


#### HTTP Status Codes

### Supported Worksheet Types

| Type         | Description                                |
| ------------ | ------------------------------------------ |
| `worksheet`  | Standard cell-based worksheet (default)    |
| `chartsheet` | Chart-only sheet                           |
| `macrosheet` | Legacy BIFF8 macro sheet                   |
| `vbmodule`   | Visual Basic for Applications (VBA) module |

> **Note**: Avoid ambiguous or deprecated types like `BIFF4Macro`, `Other`, or `Dialog`; they are not supported in v4.0.

---

## How to Use the Add Worksheet to Spreadsheet with SDKs

### Add Worksheet to Spreadsheet Specification

The [Add Worksheet to Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AddWorksheetToSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?sheetName=Q2Data&sheetType=worksheet&position=1" \
  -H "Authorization: Bearer <access_token>" \
  -H "Accept: application/json" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -o updated_workbook.xlsx
```

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{< tab tabNum="1" >}}  
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{< /tab >}}  
{{< tab tabNum="2" >}}  
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{< /tab >}}  
{{< tab tabNum="3" >}}  
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{< /tab >}}  
{{< tab tabNum="4" >}}  
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{< /tab >}}  
{{< tab tabNum="5" >}}  
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{< /tab >}}  
{{< tab tabNum="6" >}}  
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{< /tab >}}  
{{< tab tabNum="7" >}}  
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{< /tab >}}  
{{< tab tabNum="8" >}}  
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{< /tab >}}  
{{< /tabs >}}
