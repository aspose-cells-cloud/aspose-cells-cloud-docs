---
title: "Hide columns on an Excel worksheet"
second_title: "Document"
linktitle: "Hide"
type: docs
url: /columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, hide columns API, Excel column hide, REST API hide columns, Aspose.Cells SDK, spreadsheet automation"
description: "Learn how to hide one or more columns in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL example, SDK code samples, and error handling."
weight: 40
---

This REST API hides columns in a worksheet.

**Version note:** This documentation applies to Aspose.Cells Cloud API **v3.0** (latest as of 2026‑03‑30).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

The API accepts the following parameters:

| Parameter Name | Type    | Location | Description |
|----------------|---------|----------|-------------|
| name           | string  | path     | The name of the workbook file. |
| sheetName      | string  | path     | The name of the worksheet where columns will be hidden. |
| startColumn    | integer | query    | Zero‑based index of the first column to hide. |
| totalColumns   | integer | query    | Number of consecutive columns to hide, starting from **startColumn**. |
| folder         | string  | query    | Path to the folder that contains the workbook. |
| storageName    | string  | query    | Name of the storage service where the file is located. |

**Authentication:** Include the `Authorization: Bearer {access_token}` header with a valid OAuth 2.0 access token. The request must be sent over HTTPS.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services easily. The example below shows how to hide a column with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Possible response codes**

| HTTP Code | Meaning                                 | Example JSON (error)                              |
|-----------|-----------------------------------------|---------------------------------------------------|
| 200       | Success                                 | `{ "Code": 200, "Status": "OK" }`                 |
| 400       | Bad request (e.g., invalid parameters) | `{ "Code": 400, "Message": "Invalid column range." }` |
| 401       | Unauthorized (missing/invalid token)   | `{ "Code": 401, "Message": "Invalid access token." }` |
| 404       | Not found (workbook or worksheet)       | `{ "Code": 404, "Message": "File not found." }`   |
| 500       | Internal server error                   | `{ "Code": 500, "Message": "Unexpected error." }` |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your business logic. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}