---
title: "Autofit Rows on an Excel Workbook"
second_title: "Developer Guide"
linktitle: "Rows"
type: docs
url: /autofit-rows-on-an-excel-file/
aliases: [/auto-fit-rows-in-excel-workbooks/, /workbook/autofit/rows/]
keywords: "autofit rows, Excel workbook, Aspose.Cells Cloud, REST API, auto fitter options"
description: "Learn to automatically adjust row heights in an Excel workbook using Aspose.Cells Cloud REST API. Includes endpoint, parameters, cURL example, and SDK snippets for C#, Java, Python, and more."
weight: 90
ArticleTitle: "Autofit Rows on an Excel Workbook – Aspose.Cells Cloud API"
---
The **PostAutofitWorkbookRows** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows`) enables Aspose.Cells Cloud users to automatically adjust row heights in an Excel workbook to fit their contents, supporting optional range specification via `startRow`, `endRow`, `firstColumn`, and `lastColumn` query parameters. Prior to calling the API, ensure you have obtained a valid Bearer JWT token from Aspose's authentication service and that the target workbook is accessible in either the default or a configured custom storage location. The operation accepts the workbook's filename in the path and allows fine-grained control over which rows and columns to autofit, including an `onlyAuto` flag to restrict adjustments to rows already marked for auto-fitting.

This REST API enables you to **autofit rows** in an Excel workbook, automatically adjusting row height after data is inserted or modified.

## The Post Autofit Workbook Rows Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| startRow | Integer | Query | Start row. |
| endRow | Integer | Query | End row. |
| onlyAuto | Boolean | Query | Only auto. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |
| firstColumn | Integer | Query | First column index. |
| lastColumn | Integer | Query | Last column index. |

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

The request parameters include:

| Parameter Name    | Type              | Location | Description                                                                     |
| ----------------- | ----------------- | -------- | ------------------------------------------------------------------------------- |
| name              | string            | path     | Name of the workbook file.                                                      |
| autoFitterOptions | AutoFitterOptions | body     | Options that control the autofit behavior.                                      |
| startRow          | integer           | query    | Index of the first row to autofit.                                              |
| endRow            | integer           | query    | Index of the last row to autofit.                                               |
| firstColumn       | integer           | query    | Index of the first column considered for autofit.                               |
| lastColumn        | integer           | query    | Index of the last column considered for autofit.                                |
| onlyAuto          | boolean           | query    | If **true**, only rows with the AutoFit flag are processed (default **false**). |
| folder            | string            | query    | Folder path where the workbook is stored.                                       |
| storageName       | string            | query    | Name of the storage service.                                                    |

**AutoFitterOptions** is an object that specifies how the autofit operation behaves (e.g., `AutoFitMergedCells`, `IgnoreHidden`).


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to call Aspose.Cells web services. Replace `<jwt token>` with a valid Bearer JWT token obtained from the Aspose authentication service.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

_Example error response (e.g., missing workbook):_

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "The specified workbook 'myWorkbook.xlsx' does not exist."
}
```

{{< /tab >}}

{{< /tabs >}}

**Notes**

- When `AutoFitMergedCells` is set to **true**, merged cells are considered as a single entity during the autofit operation.
- Setting `IgnoreHidden` to **true** skips hidden rows and columns, preserving their current dimensions.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
