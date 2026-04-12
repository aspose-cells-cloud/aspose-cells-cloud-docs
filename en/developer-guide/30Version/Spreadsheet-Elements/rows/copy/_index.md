---
title: "Copy Rows on an Excel Worksheet"
second_title: "Document"
linktitle: "Copy"
type: docs
url: /rows/copy/
aliases: [/copy-rows-in-excel-worksheet/]
keywords: "Aspose.Cells Cloud Copy Rows, Excel, Aspose.Cells Cloud, REST API, worksheet rows"
description: "Learn how to copy rows in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes authentication steps, request/response details, error handling, and SDK examples."
weight: 30
---

This REST API copies rows within a worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

### **Request parameters**

| Parameter Name      | Type    | Location | Description                                                           |
| ------------------- | ------- | -------- | --------------------------------------------------------------------- |
| name                | string  | path     | The workbook file name.                                               |
| sheetName           | string  | path     | The worksheet name.                                                   |
| sourceRowIndex      | integer | query    | Zero‑based index of the source row.                                   |
| destinationRowIndex | integer | query    | Zero‑based index where the rows will be placed.                       |
| rowNumber           | integer | query    | Number of rows to copy.                                               |
| worksheet           | string  | query    | _(Optional)_ Worksheet identifier; usually the same as **sheetName**. |
| folder              | string  | query    | Path to the folder containing the document.                           |
| storageName         | string  | query    | Name of the storage service.                                          |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Error Handling

| HTTP Code | Meaning                                             | Example Error Body                                            |
| --------- | --------------------------------------------------- | ------------------------------------------------------------- |
| 400       | Bad Request – missing or invalid parameters         | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }`       |
| 401       | Unauthorized – invalid or missing JWT token         | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404       | Not Found – workbook or worksheet does not exist    | `{ "Code": 404, "Message": "File not found." }`               |
| 500       | Internal Server Error – unexpected server condition | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

Handle these responses by checking the HTTP status code and parsing the JSON error object for `Code` and `Message`.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details, allowing you to focus on your project logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
