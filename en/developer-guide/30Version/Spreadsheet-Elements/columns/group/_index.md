---
title: "Group columns on an Excel worksheet"
second_title: "Document"
linktitle: "Group"
type: docs
url: /columns/group/
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
keywords: "Aspose.Cells Cloud, group columns, Excel API, REST, SDK, spreadsheet"
description: "Learn how to group columns in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes cURL, SDK examples, parameters, and response details."
weight: 60
---

This REST API **lets you** group worksheet columns.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

### Request Parameters

| Parameter Name | Type    | Location | Description                                                                 |
| -------------- | ------- | -------- | --------------------------------------------------------------------------- |
| name           | string  | path     | Name of the workbook file.                                                  |
| sheetName      | string  | path     | Name of the worksheet containing the columns.                               |
| firstIndex     | integer | query    | Zero‑based index of the first column to group.                              |
| lastIndex      | integer | query    | Zero‑based index of the last column to group.                               |
| hide           | boolean | query    | If **true**, the grouped columns are hidden; otherwise they remain visible. |
| folder         | string  | query    | Path to the folder that contains the workbook.                              |
| storageName    | string  | query    | Name of the storage service where the file is located.                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

### cURL Example

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

### Success Response

| Field  | Type    | Description                                     |
| ------ | ------- | ----------------------------------------------- |
| Code   | integer | HTTP status code (200 for success).             |
| Status | string  | Textual status of the operation (e.g., **OK**). |

### Error Response

When the request fails, the API returns additional fields describing the error.

| Field        | Type    | Description                                          |
| ------------ | ------- | ---------------------------------------------------- |
| Code         | integer | HTTP status code (e.g., 400, 401, 404, 500).         |
| Status       | string  | Textual status (e.g., **Error**).                    |
| ErrorMessage | string  | Human‑readable description of the problem.           |
| ErrorCode    | string  | Specific error identifier for programmatic handling. |

## Cloud SDK Family

Using an SDK is the fastest way to develop with Aspose.Cells Cloud. An SDK handles low‑level details so you can focus on your business logic. For a complete list of supported SDKs, see the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
