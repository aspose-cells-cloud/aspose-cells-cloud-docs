---
title: "Freeze Panes on an Excel Worksheet"
second_title: "Document"
linktitle: "Freeze"
type: docs
url: /worksheets/panes/freeze/
aliases: [/freeze-panes-in-excel-worksheet/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, Freeze Panes, Excel, REST API, Worksheet"
description: "Learn how to freeze rows and columns in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes endpoint syntax, required parameters, a cURL example, authentication guidance, error‑response details, and SDK code samples for multiple languages."
weight: 190
---

This REST API **sets** freeze panes on an Excel worksheet.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

The request parameters are:

| Parameter Name | Type    | Location | Description                                         |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name           | string  | path     | The name of the workbook file.                      |
| sheetName      | string  | path     | The name of the worksheet where panes are frozen.   |
| row            | integer | query    | Zero‑based index of the first **unfrozen** row.     |
| column         | integer | query    | Zero‑based index of the first **unfrozen** column.  |
| frozenRows     | integer | query    | Number of rows to freeze starting from the top.     |
| frozenColumns  | integer | query    | Number of columns to freeze starting from the left. |
| folder         | string  | query    | Folder path in storage where the workbook resides.  |
| storageName    | string  | query    | Name of the storage service.                        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### Error‑Response

| HTTP Status               | Code | Message                         | Example                                                  |
| ------------------------- | ---- | ------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400  | Invalid parameters              | `{ "Code": 400, "Message": "Invalid frozenRows value" }` |
| 401 Unauthorized          | 401  | Missing or invalid JWT token    | `{ "Code": 401, "Message": "Invalid access token" }`     |
| 404 Not Found             | 404  | Workbook or worksheet not found | `{ "Code": 404, "Message": "File not found" }`           |
| 500 Internal Server Error | 500  | Unexpected server error         | `{ "Code": 500, "Message": "Internal server error" }`    |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}
