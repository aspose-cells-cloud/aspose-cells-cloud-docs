---
title: "Set Cell Formula in Excel Worksheets"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, Set Formula, Worksheet, Cell, Cloud SDK, cURL"
description: "Set Excel cell formulas using Aspose.Cells Cloud REST API with cURL or SDKs (C#, Java, Python, etc.)."
linktitle: "Set Cell Formula"
ArticleTitle: "Set Formula for a Cell in Excel Using Aspose.Cells Cloud REST API"
---

The **PostWorksheetCellSetValue** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}`) enables developers to set a formula or value for a specific cell in an Excel worksheet using its cell name via Aspose.Cells Cloud, supporting operations like assigning dynamic formulas such as `=SUM(A1:A10)` directly to cells without local Excel installation.

## The Post Worksheet Cell Set Value Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------ | -------------------------- | -------------------------------------------- |
| name           | String | Path                       | The file name.                               |
| sheetName      | String | Path                       | The worksheet name.                          |
| cellName       | String | Path                       | The cell name.                               |
| value          | String | Query                      | The cell value.                              |
| type           | String | Query                      | The value type.                              |
| formula        | String | Query                      | Formula for cell                             |
| folder         | String | Query                      | The folder where the file is situated.       |
| storageName    | String | Query                      | The storage name where the file is situated. |

### Response

```json
[
  {
    "Name": "CellResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellResponse"
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
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

Return CellResponse.

- **Response Fields Overview**

| Field           | Type    | Description                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Address of the cell (e.g., `F341`).                   |
| `Row`           | integer | Zero‑based row index.                                 |
| `Column`        | integer | Zero‑based column index.                              |
| `Value`         | string  | The cell’s displayed value.                           |
| `Type`          | string  | Data type of the cell (e.g., `IsString`).             |
| `Formula`       | string  | Formula text if the cell contains a formula.          |
| `IsFormula`     | bool    | Indicates whether the cell contains a formula.        |
| `IsMerged`      | bool    | Indicates whether the cell is part of a merged range. |
| `IsArrayHeader` | bool    | Indicates whether the cell is an array header.        |
| `IsInArray`     | bool    | Indicates whether the cell belongs to an array.       |
| `IsErrorValue`  | bool    | Indicates whether the cell contains an error value.   |
| `IsInTable`     | bool    | Indicates whether the cell is inside a table.         |
| `IsStyleSet`    | bool    | Indicates whether a style is applied to the cell.     |
| `HtmlString`    | string  | HTML‑encoded representation of the cell’s value.      |
| `Style.link`    | object  | Hyperlink to the style resource.                      |

## How to Use the Post Worksheet Cell Set Value API with SDKs?

### Post Worksheet Cell Set Value API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue" rel="noopener noreferrer">Post Worksheet Cell Set Value API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### curl Example

Use the cURL command‑line tool to call Aspose.Cells web services.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}
{{</tab>}}
{{< /tabs >}}
