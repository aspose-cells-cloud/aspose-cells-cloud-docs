---
title: "Autofit Multiple Rows in an Excel Worksheet"
second_title: "Document"
linktitle: "Rows"
type: docs
url: /worksheets/autofit/rows/
aliases: [/autofit-multiple-rows-of-worksheet/]
keywords: "autofit rows Excel, Aspose.Cells Cloud, REST API, worksheet, spreadsheet"
description: "Learn how to use the Aspose.Cells Cloud REST API to autofit multiple rows in an Excel worksheet. Includes request syntax, parameters, cURL example, SDK snippets, and error handling."
weight: 40
---

This REST API automatically adjusts the height of rows in an Excel worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

**Authentication** – Obtain a JWT token from the `/connect/token` endpoint and include it in the request header as `Authorization: Bearer <token>`.

The request parameters are:

| Parameter Name       | Type    | Location | Description                                                                                                                            | Required |
|----------------------|---------|----------|----------------------------------------------------------------------------------------------------------------------------------------|----------|
| **name**             | string  | path     | The name of the Excel file.                                                                                                            | ✔︎ |
| **sheetName**        | string  | path     | The name of the worksheet.                                                                                                             | ✔︎ |
| **autoFitterOptions**| object  | body     | Options that control how rows are autofitted (e.g., ignore hidden rows). See the brief field description below.                        | ✘ |
| **startRow**         | integer | query    | The first row to autofit (1-based index).                                                                                              | ✔︎ |
| **endRow**           | integer | query    | The last row to autofit (inclusive).                                                                                                   | ✔︎ |
| **onlyAuto**         | boolean | query    | When `true`, the API adjusts only rows whose height is automatically calculated by Excel. When `false`, a full autofit is performed. | ✘ |
| **folder**           | string  | query    | The folder that contains the document.                                                                                                 | ✘ |
| **storageName**      | string  | query    | The name of the storage service.                                                                                                       | ✘ |

**autoFitterOptions** fields (all optional):

- `AutoFitMergedCells` *(boolean)* – If `true`, merged cells are taken into account when calculating row height.  
- `IgnoreHidden` *(boolean)* – When `true`, hidden rows are ignored during the autofit process.  
- `OnlyAuto` *(boolean)* – Mirrors the query‑parameter `onlyAuto`; when set, it overrides the query value.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Typical error responses include:

- **400 Bad Request** – Invalid parameter values or malformed JSON body.  
- **401 Unauthorized** – Missing or invalid JWT token.  
- **404 Not Found** – The specified file or worksheet does not exist.  
- **500 Internal Server Error** – An unexpected server error occurred.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}