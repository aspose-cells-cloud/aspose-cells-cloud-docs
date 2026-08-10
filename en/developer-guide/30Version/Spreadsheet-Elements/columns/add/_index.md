---
title: "Add an Empty Column to an Excel Worksheet - Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Add"
type: docs
url: /columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "add, column, Excel, API, Aspose.Cells, Cloud, REST, insert"
description: "Learn how to insert a new column into an Excel sheet using Aspose.Cells Cloud REST API. Includes request syntax, cURL example, and SDK code samples."
weight: 20
ArticleTitle: "Add Empty Column to Excel Worksheet Using Aspose.Cells Cloud API"
---

This REST API inserts one or more columns into a worksheet.  

**Prerequisites**  
Before calling this endpoint, ensure you have completed the following steps:

- Obtain a valid OAuth 2.0 access token and include it in the `Authorization` header.  
- Store the target workbook in the selected storage (default = “Default”) or specify the appropriate `folder` and `storageName` parameters.  
- Verify that the worksheet name provided in `sheetName` exists in the workbook.

## PutInsertWorksheetColumns API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name      | Type    | Location | Description                                                          |
| ------------------- | ------- | -------- | -------------------------------------------------------------------- |
| **name**            | string  | path     | The workbook file name.                                              |
| **sheetName**       | string  | path     | The worksheet name.                                                  |
| **columnIndex**     | integer | path     | Zero‑based index of the column where insertion begins.               |
| **totalColumns**    | integer | query    | Number of columns to insert.                                         |
| **updateReference** | boolean | query    | When **true**, cell references are updated to reflect the insertion. |
| **folder**          | string  | query    | Path to the folder containing the workbook.                          |
| **storageName**     | string  | query    | Name of the storage service.                                         |

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

| Code | Description                                 |
|------|---------------------------------------------|
| 200  | Column(s) inserted successfully.            |
| 400  | Bad request – missing or invalid parameters.|
| 401  | Unauthorized – invalid or missing token.    |
| 404  | Workbook or worksheet not found.            |
| 500  | Internal server error.                      |

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