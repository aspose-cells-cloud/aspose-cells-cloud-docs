---
title: "Export a Worksheet Page – Aspose.Cells Cloud API Reference"
ArticleTitle: "Export a Worksheet Page – Aspose.Cells Cloud API Reference"
second_title: "Document"
linktitle: "Page"
type: docs
url: /worksheets/page-to-different-formats/
aliases: [/get-worksheet-for-page-index/]
keywords: "Aspose.Cells Cloud, worksheet page export, PDF, PNG, CSV, REST API, JWT authentication, file formats"
description: "Learn how to export a specific worksheet page to PDF, PNG, CSV, and more using Aspose.Cells Cloud REST API. Includes cURL request, parameter guide, and SDK samples for multiple languages."
weight: 240
---

Exporting a specific worksheet page is useful when you need a printable snapshot of a report, a chart image, or a data extract without downloading the entire workbook. This endpoint lets you retrieve a single page in the format that best fits your downstream workflow.

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API lets you convert a specified page of a worksheet to various file formats. Supported formats: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) defines a publicly accessible programming interface and enables you to perform REST interactions directly from a web browser.

> **Prerequisites** – You must have a valid JWT authentication token and the workbook stored in a cloud folder that you specify with the `folder` parameter.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Response** – The service returns the requested page in the chosen format. For image formats (png, jpeg, gif, etc.) the body contains the binary image; for document formats (pdf, xls, csv, …) the body contains the file content. A successful call returns HTTP 200.

*Example of a PNG response (truncated base64 snippet):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Parameters**

| Parameter              | Type    | Description                                                          | Default |
| ---------------------- | ------- | -------------------------------------------------------------------- | ------- |
| `format`               | string  | Output file format (e.g., `pdf`, `png`, `csv`).                      | `pdf`   |
| `verticalResolution`   | integer | Vertical DPI of the rendered image.                                  | `100`   |
| `horizontalResolution` | integer | Horizontal DPI of the rendered image.                                | `100`   |
| `pageIndex`            | integer | Zero‑based index of the worksheet page to export (`0` = first page). | `0`     |
| `folder`               | string  | Cloud storage folder where the source workbook resides.              | —       |

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

**Possible errors**

- **401 Unauthorized** – Invalid or missing JWT token.
- **404 Not Found** – Specified workbook or worksheet does not exist.
- **400 Bad Request** – Invalid parameter value (e.g., unsupported `format`).
- **500 Internal Server Error** – Unexpected server‑side problem.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}