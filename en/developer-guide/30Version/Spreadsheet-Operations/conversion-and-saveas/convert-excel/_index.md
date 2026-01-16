---
title: "Convert an Excel File to Different Formats"
second_title: "Document"
linktitle: "Convert Excel"
type: docs
url: /convert-an-excel-file-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/,/convert/excel-to-different-formats/]
keywords: "Aspose.Cells Cloud, Excel conversion, REST API, workbook format conversion, CSV, PDF, HTML, JSON, Markdown"
description: "Use Aspose.Cells Cloud REST API to convert Excel workbooks to a variety of formats such as CSV, PDF, HTML, JSON, and more. Supports multiple SDKs for popular programming languages."
weight: 10
---

This REST API converts an Excel file to different output formats.

The request is an HTTP **PUT** with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart body contains the **data file**, and the second part contains the **save options**.

### Query Parameters

| Parameter Name            | Type   | Description |
|---------------------------|--------|-------------|
| `format`                  | string | Target file format (e.g., CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). |
| `password`                | string | Password required to open the source Excel file. |
| `outPath`                 | string | Full path (including filename and extension) for a single output file, or folder path when multiple files are generated. |
| `storageName`             | string | Name of the storage where the source file resides. |
| `checkExcelRestriction`  | bool   | When **true**, validates Excel restrictions before modifying cells or related objects. |
| `streamFormat`            | string | Format of the input file stream. |
| `region`                  | string | Regional settings applied to the workbook. |
| `pageWideFitOnPerSheet`   | bool   | Adjusts page width to fit each worksheet when converting to PDF. |
| `pageTallFitOnPerSheet`   | bool   | Adjusts page height to fit each worksheet when converting to PDF. |
| `sheetName`               | string | Name of the worksheet to convert. |
| `pageIndex`               | string | Index of the page to convert (requires `sheetName`). |
| `onePagePerSheet`         | bool   | When **true**, generates one PDF page per worksheet. |
| `AutoRowsFit`             | bool   | Auto‑fits all rows in the workbook. |
| `AutoColumnsFit`          | bool   | Auto‑fits column widths in the workbook. |

### Request Body Parameters

| Parameter Name | Type      | Description |
|----------------|-----------|-------------|
| `datafile`     | data file | The Excel file placed in the first part of the multipart body. |
| `SaveOptions`  | object    | Save options placed in the second part of the multipart body. |

## REST API

| API                | Type | Description                                            | Swagger Link |
|--------------------|------|--------------------------------------------------------|--------------|
| `/cells/convert`   | PUT  | Converts a workbook from request content to the chosen format. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) defines a publicly accessible interface that enables direct REST interactions from a web browser.

### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

## Cloud SDK Family

Using an SDK accelerates development by handling low‑level details, allowing you to focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}