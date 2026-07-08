---
title: "Unhide an Excel worksheet"
second_title: "Document"
linktitle: "Unhide"
type: docs
url: /worksheets/unhide/
aliases: [/unhide-excel-worksheets/]
keywords: "Aspose.Cells, unhide worksheet, Excel API, cloud spreadsheet, REST, worksheet visibility, Excel workbook"
description: "Learn how to use Aspose.Cells Cloud REST API to unhide a worksheet in an Excel workbook. Includes request details, cURL examples, and SDK code snippets for multiple programming languages."
weight: 60
---

This REST API provides an endpoint to **unhide a worksheet** in an Excel workbook.

**Prerequisites**  
Before calling this operation you must have:

* A valid Aspose Cloud access token (JWT) included in the `Authorization` header.  
* The workbook stored in a supported storage location that you specify with the `folder` and `storageName` query parameters.  
* The workbook must be in a format supported by Aspose.Cells (e.g., `.xls`, `.xlsx`, `.xlsm`).  

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **Request parameters**

| Parameter Name | Type    | Location | Description                              |
| -------------- | ------- | -------- | ---------------------------------------- |
| name           | string  | path     | Document name.                           |
| sheetName      | string  | path     | Worksheet name.                          |
| isVisible      | boolean | query    | New worksheet visibility value (`true`). |
| folder         | string  | query    | The document folder.                     |
| storageName    | string  | query    | Storage name.                            |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) defines a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to call Aspose.Cells web services easily. The example below shows how to make a request with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # replace <jwt token> with your access token
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Possible response codes**

| HTTP Code | Meaning                              | Sample Body (when applicable)                               |
|-----------|--------------------------------------|--------------------------------------------------------------|
| 200       | Worksheet visibility updated successfully | `{ "Code": 200, "Status": "OK" }`                           |
| 400       | Bad request – missing or invalid parameters | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401       | Unauthorized – missing or invalid JWT token | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404       | Not found – workbook or worksheet does not exist | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500       | Internal server error                | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}