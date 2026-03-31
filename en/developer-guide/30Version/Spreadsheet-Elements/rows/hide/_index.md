---
title: "Hide rows on an Excel worksheet"
second_title: "Document"
linktitle: "Hide"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "hide rows, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Learn how to hide one or multiple rows in an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL example, SDK snippets, parameters, authentication, response details, and error handling."
weight: 40
---

This REST API hides rows on an Excel worksheet.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### Request parameters

| Parameter      | Type    | Location | Description |
|----------------|---------|----------|-------------|
| **name**       | string  | path     | The name of the workbook file. |
| **sheetName**  | string  | path     | The name of the worksheet containing the rows to hide. |
| **startrow**   | integer | query    | Zero‑based index of the first row to be hidden. |
| **totalRows**  | integer | query    | The number of consecutive rows to hide, starting from **startrow**. |
| **folder**     | string  | query    | The folder in storage where the workbook is located. |
| **storageName**| string  | query    | The name of the storage service. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) defines a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The API requires a JWT Bearer token obtained from the Aspose Cloud OAuth endpoint; include it in the `Authorization` header. The example below demonstrates how to hide a row using cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
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

A successful call returns a JSON object that contains the fields `Code` and `Status`. In case of an error, the response includes additional fields such as `Message` and appropriate HTTP status codes (e.g., 400, 401, 404, 500).

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality into your application. SDKs handle low‑level details so you can focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to hide rows using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}