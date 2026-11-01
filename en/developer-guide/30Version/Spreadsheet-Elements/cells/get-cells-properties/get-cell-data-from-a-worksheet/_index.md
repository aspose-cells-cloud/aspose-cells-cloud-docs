---
title: "Get Cell Data from a Worksheet"
type: docs
url: /get-cell-data-from-a-worksheet/
weight: 100
date: 2024-06-15
api_version: "3.0"
keywords: "Aspose.Cells Cloud, get cell data, Excel API, REST API, cell value, worksheet API, Aspose API example"
description: "Get cell value, type, and style from an Excel worksheet using Aspose.Cells Cloud REST API v3.0 with cURL or SDKs"
ArticleTitle: "Get Cell Data from a Worksheet"
linktitle: "Get Cell Data"
---
The **GetWorksheetCell** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}`) retrieves cell data from a specific worksheet in an Excel file using either a cell reference (e.g., `A3`) or a predefined method name (e.g., `firstcell`, `endcell`), enabling developers to programmatically extract cell content via Aspose.Cells Cloud's REST interface.

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

- **cURL Example**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3" \
     -H "Authorization: Bearer <access_token>¹" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parameters**

| Parameter          | Type   | Description                                                                         | Required |
| ------------------ | ------ | ----------------------------------------------------------------------------------- | -------- |
| `cellOrMethodName` | string | Must match the cell address (e.g., `A3`) or method (e.g., `firstcell`, `lastcell`). | Yes      |
| `fileName`         | string | Name of the workbook file (e.g., `myWorkbook.xlsx`).                                | Yes      |
| `worksheet`        | string | Name of the worksheet (e.g., `Sheet1`).                                             | Yes      |
| `Authorization`    | header | Bearer token for authentication.                                                    | Yes      |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

> _Note: `IsStyleSet` is deprecated in v3.1+; use `Style` object instead._

{{< /tab >}}

{{< /tabs >}}

- **Use Aspose.Cells Cloud SDKs**

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="TypeScript" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

¹ Obtain your access token via [OAuth 2.0 authentication](/oauth2-authentication/).
