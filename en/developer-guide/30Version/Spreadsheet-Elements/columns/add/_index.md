---
title: "Add an Empty Column to an Excel Worksheet - Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Add"
type: docs
url: /columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "add, column, Excel, API, Aspose.Cells, Cloud, REST, insert"
description: "Insert one or more columns into an Excel worksheet using Aspose.Cells Cloud REST API with cURL or SDK examples."
weight: 100
ArticleTitle: "Add Empty Column to Excel Worksheet Using Aspose.Cells Cloud API"
---
The **PutInsertWorksheetColumns** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`) inserts one or more columns into a specified worksheet at a given column index, using Aspose.Cells Cloud to programmatically manage spreadsheet structure. It requires the file name, worksheet name, column index, and number of columns to insert, with optional control over reference updates and storage location. This operation supports dynamic worksheet expansion while maintaining formatting and formula integrity across the workbook.

## The Put Insert Worksheet Columns Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| columnIndex | Integer | Path | The column index. |
| columns | Integer | Query | The number of columns. |
| updateReference | Boolean | Query | Indicates if references in other worksheets will be updated. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Notes**

- The `columnIndex` must be between 0 and the current number of columns in the worksheet. Inserting beyond the existing range will automatically expand the sheet.
- Inserting multiple columns (`totalColumns` > 1) shifts existing columns to the right.
- The `updateReference` flag defaults to `false`; set to `true` to update formulas and named ranges.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to call Aspose.Cells web services. The following example shows a complete request, including authentication and the correct path parameter.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Response codes**


**Example error responses**

```json
// 400 Bad Request – missing or invalid parameters
{
  "Code": 400,
  "Message": "Invalid parameter: totalColumns must be a positive integer."
}

// 401 Unauthorized – invalid or missing token
{
  "Code": 401,
  "Message": "Authentication failed. Access token is missing or invalid."
}

// 404 Not Found – workbook or worksheet does not exist
{
  "Code": 404,
  "Message": "Workbook 'test.xlsx' not found."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "An unexpected error occurred on the server."
}
```

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
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

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project logic. See the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
