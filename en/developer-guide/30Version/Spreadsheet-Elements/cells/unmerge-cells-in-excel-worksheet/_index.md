---
title: "Unmerge Cells in Excel Worksheet"
type: docs
url: /unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, Unmerge Cells, REST API, Cloud SDK"
description: "Learn how to use the Aspose.Cells Cloud REST API to unmerge cells in an Excel worksheet, with request examples, response format, and SDK code samples for multiple programming languages."
ArticleTitle: "Unmerge Cells in Excel Worksheet"
---

This REST API unmerges cells in an Excel file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Request parameters**

| Parameter Name | Type    | Location | Description                                             |
|----------------|---------|----------|---------------------------------------------------------|
| name           | string  | path     | Name of the workbook file.                              |
| sheetName      | string  | path     | Name of the worksheet.                                  |
| startRow       | integer | query    | Zero‑based index of the first row to unmerge.           |
| startColumn    | integer | query    | Zero‑based index of the first column to unmerge.        |
| totalRows      | integer | query    | Number of rows to include in the unmerge operation.    |
| totalColumns   | integer | query    | Number of columns to include in the unmerge operation. |
| folder         | string  | query    | Folder path where the workbook is stored.               |
| storageName    | string  | query    | Name of the storage service.                            |

## **Response**

Return CellCloudResponse.

- **Response Fields Overview**

| Field           | Type    | Description                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                    |
| `Code`           | integer | 200,400,401,500,...                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the PostWorksheetUnmerge API with SDKs

### PostWorksheetUnmerge API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}