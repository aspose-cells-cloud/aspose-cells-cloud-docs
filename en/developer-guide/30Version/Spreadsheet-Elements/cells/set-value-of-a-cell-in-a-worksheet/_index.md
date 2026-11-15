---
title: "Set Cell Value in Worksheet – Aspose.Cells Cloud REST API v3.0"
date: 2024-05-15
tags:
  - rest-api
  - excel
  - cell-update
  - cells-cloud
categories:
  - api-reference
  - aspose-cells
weight: 70
description: "Aspose.Cells Cloud REST API v3.0: Set Excel cell values via POST /cells/{name}/worksheets/{sheetName}/cells/{cellName}. Includes cURL, .NET, Java, Python, and Node.js examples."
---

The **PostWorksheetCellSetValue** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}`) enables developers to programmatically set a cell's value, formula, or type in an Excel worksheet using Aspose.Cells Cloud, supporting strings, numbers, and formulas via simple path and query parameters.

> 📝 **Note**: This documentation covers Aspose.Cells Cloud API v3.0. For the latest features, see the [v4.0 Preview](/total/getting-started/v4-preview/). Always verify SDK version compatibility before integration.

## The Post Worksheet Cell Set Value Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

### Security and Authentication

All requests require a valid [JWT token](/total/getting-started/rest-api-overview/authenticating-api-requests/) in the `Authorization` header:

```http
Authorization: Bearer <your-jwt-token>
```

### Path Parameters

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

### Query Parameters

| Parameter     | Type   | Required | Description                                                                                                  |
| ------------- | ------ | -------- | ------------------------------------------------------------------------------------------------------------ |
| `value`       | string | No       | The value to assign to the cell.                                                                             |
| `type`        | string | No       | Data type of `value`: `int`, `string`, `float`, `bool`, `date`, `duration`. Defaults to `string` if omitted. |
| `formula`     | string | No       | A formula to assign (e.g., `=SUM(A2:A15)`). Overrides `value` if both provided.                              |
| `folder`      | string | No       | Folder path containing the file (e.g., `/docs/`).                                                            |
| `storageName` | string | No       | Custom storage name (e.g., `First Storage`).                                                                 |

> ⚠️ **Security Note**: Replace `<jwt token>` with your actual JWT token (see [Authentication](/total/getting-started/rest-api-overview/authenticating-api-requests/)). Never commit tokens to source control, logs, or public repositories.

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9..."
```

> ✅ **Tip**: Use the [Aspose.Cells Cloud Dashboard](https://dashboard.aspose.cloud/) to generate and manage your client credentials and tokens securely.

## Response

Returns a `CellResponse` object with HTTP status `200 OK` on success.

### CellResponse Fields

| Field           | Type    | Description                                         |
| --------------- | ------- | --------------------------------------------------- |
| `Name`          | string  | Cell address (e.g., `A3`).                          |
| `Row`           | integer | Zero-based row index.                               |
| `Column`        | integer | Zero-based column index.                            |
| `Value`         | string  | Displayed cell value.                               |
| `Type`          | string  | Internal type (e.g., `IsString`, `IsNumeric`).      |
| `Formula`       | string  | Formula text (if present).                          |
| `IsFormula`     | bool    | `true` if the cell contains a formula.              |
| `IsMerged`      | bool    | `true` if part of a merged range.                   |
| `IsArrayHeader` | bool    | `true` if cell is an array formula header.          |
| `IsInArray`     | bool    | `true` if cell belongs to an array formula.         |
| `IsErrorValue`  | bool    | `true` if cell contains an error (e.g., `#DIV/0!`). |
| `IsInTable`     | bool    | `true` if cell is inside an Excel table.            |
| `IsStyleSet`    | bool    | `true` if a custom style is applied.                |
| `HtmlString`    | string  | HTML-formatted representation of the value.         |
| `Style.link`    | object  | Link to the cell’s style resource.                  |

### Example Response (200 OK)

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "1234",
    "Type": "IsNumeric",
    "Formula": null,
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "1234",
    "Style": {
      "link": {
        "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/styles/0",
        "Rel": "self",
        "Type": "application/json"
      }
    }
  }
}
```

## How to Use the Post Worksheet Cell Set Value API with SDKs?

### Post Worksheet Cell Set Value API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue" rel="noopener noreferrer">Post Worksheet Cell Set Value API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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
