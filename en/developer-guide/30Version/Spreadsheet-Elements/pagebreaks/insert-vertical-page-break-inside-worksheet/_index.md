---
title: "Add a Vertical Page Break"
second_title: "Document"
linktitle: "Add a Vertical Page Break"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, vertical page break, REST API, Excel, SDK, cURL, add page break"
description: "Learn how to insert a vertical page break into an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes request syntax, cURL example, SDK samples, authentication guide, and error‑handling details."
weight: 40
---

This REST API inserts a vertical page break into a worksheet.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Request Parameters

| Parameter Name | Type    | Location | Description                                                             |
| -------------- | ------- | -------- | ----------------------------------------------------------------------- |
| name           | string  | path     | The name of the Excel workbook.                                         |
| sheetName      | string  | path     | The name of the worksheet where the page break will be added.           |
| cellname       | string  | query    | The cell reference (e.g., **A1**) that defines the page‑break location. |
| column         | integer | query    | The zero-based index of the column where the page break starts.         |
| row            | integer | query    | The zero-based index of the row where the page break starts.            |
| startRow       | integer | query    | The first row of the page‑break range.                                  |
| endRow         | integer | query    | The last row of the page‑break range.                                   |
| folder         | string  | query    | The folder path in the storage where the workbook is located.           |
| storageName    | string  | query    | The name of the storage service.                                        |

**Required parameters** – Either `cellname` **or** `column` must be supplied. When `column` is used you may also provide `row`, `startRow`, and `endRow` to define a range. All other fields are optional.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Error Codes

| HTTP Status | Description                                       | Sample Error JSON                                             |
| ----------- | ------------------------------------------------- | ------------------------------------------------------------- |
| 400         | Bad request – missing or invalid parameters.      | `{ "Code": 400, "Message": "Invalid parameter: column" }`     |
| 401         | Unauthorized – invalid or missing JWT token.      | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404         | Not found – workbook or worksheet does not exist. | `{ "Code": 404, "Message": "File not found." }`               |
| 500         | Internal server error – unexpected condition.     | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}
