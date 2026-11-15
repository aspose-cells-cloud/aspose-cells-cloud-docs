---
title: Get Column Details – Aspose.Cells Cloud API Reference (v3.0)
linktitle: "Get"
type: docs
url: /get-column-details/
aliases:
  [
    /get-columns-from-an-excel-worksheet/,
    /get-columns-from-a-worksheet/,
    /get-column-from-a-worksheet/,
  ]
linkTitle: "Get Column Details"
weight: 100
ArticleTitle: "Get Column Details API - Aspose.Cells Cloud REST v3.0"
description: "Retrieve Excel column metadata—index, width, hidden state, style—via Aspose.Cells Cloud REST API v3.0."
keywords: "Aspose.Cells Cloud, get column details, Excel column metadata, REST API v3.0, column width, hidden column, column index, worksheet API, GetWorksheetColumns"
---

The **GetWorksheetColumn** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`) retrieves detailed column metadata—including index, width, hidden state, and style—from an Excel worksheet using the Aspose.Cells Cloud REST API v3.0, enabling developers to programmatically inspect and work with specific column properties by passing the file name, worksheet name, and zero-based column index as required path parameters.

## The Get Worksheet Column Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------- | -------------------------- | -------------------------------------------- |
| name           | String  | Path                       | The file name.                               |
| sheetName      | String  | Path                       | The worksheet name.                          |
| columnIndex    | Integer | Path                       | The column index.                            |
| folder         | String  | Query                      | The folder where the file is situated.       |
| storageName    | String  | Query                      | The storage name where the file is situated. |

> **Important:** While the specification marks `name`, `sheetName`, and `columnIndex` as `Required: false`, these are _functionally required_ for a valid request. Omitting them will result in a `400 Bad Request`.

### Response

```json
[
  {
    "Name": "ColumnResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "ColumnResponse"
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

- **{name}** – workbook file name (e.g., `test.xlsx`).
- **{sheetName}** – worksheet name (e.g., `Sheet1`).
- **{columnIndex}** – zero‑based index of the column to retrieve.

## Response Example

```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

## Response Schema

| Field               | Type    | Description                                        |
| ------------------- | ------- | -------------------------------------------------- |
| `Column.GroupLevel` | integer | Outline level of the column (used for grouping).   |
| `Column.Index`      | integer | Zero‑based index of the column.                    |
| `Column.IsHidden`   | boolean | `true` if the column is hidden; otherwise `false`. |
| `Column.Width`      | number  | Width of the column expressed in characters.       |
| `Column.Style`      | object  | Contains a `link` to the column’s style resource.  |
| `Column.link`       | object  | Self‑link to the column resource.                  |
| `Code`              | integer | HTTP status code of the response.                  |
| `Status`            | string  | Textual description of the status (e.g., **OK**).  |

### Example – 404 Not Found

```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### Example – 401 Unauthorized

```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

## How to Use the Get Worksheet Column API with SDKs?

### Get Worksheet Column API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/GetWorksheetColumn" rel="noopener noreferrer">Get Worksheet Column API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

## cURL Example

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetColumn.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetColumn.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetColumn.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetColumn.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetColumn.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetColumn.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetColumn.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetColumn.go" >}}
{{</tab>}}
{{< /tabs >}}
