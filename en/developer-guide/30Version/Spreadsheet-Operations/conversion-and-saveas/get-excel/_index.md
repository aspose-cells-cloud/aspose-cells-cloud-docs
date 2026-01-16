---
title: "Get Excel file to other formats"
second_title: "Document"
linktitle: "Get Excel"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel conversion, CSV, PDF, HTML, ODS, JSON, image formats, spreadsheet export"
description: "Aspose.Cells Cloud REST API enables converting Excel workbooks to a wide range of formats such as CSV, PDF, HTML, ODS, JSON, and various image types. SDKs are available for many programming languages, including Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 10
---

This REST API retrieves an Excel workbook in a different format.

**Query Parameters**

| Parameter Name            | Type   | Description                                                                                                                                                     |
|---------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format                    | string | Target file format (e.g., CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). |
| password                  | string | Password required to open the Excel file.                                                                                                                       |
| isAutoFit                 | bool   | Automatically fits rows and columns width. Default is **false**.                                                                                               |
| onlySaveTable             | bool   | When **true**, only table data is saved. Accepts `true` or `false`.                                                                                             |
| outPath                   | string | Path to save the result. For a single file, include the filename and extension; for multiple files, specify only the folder.                                   |
| outStorageName            | string | Name of the storage where the output file will be saved.                                                                                                        |
| checkExcelRestriction     | bool   | Checks Excel restrictions when modifying cells or related objects.                                                                                              |
| region                    | string | Regional settings applied to the workbook.                                                                                                                      |
| pageWideFitOnPerSheet     | bool   | Fits the page width to each worksheet when converting to PDF.                                                                                                   |
| pageTallFitOnPerSheet     | bool   | Fits the page height to each worksheet when converting to PDF.                                                                                                  |
| onePagePerSheet           | bool   | Generates one PDF page per worksheet.                                                                                                                            |
| folder                    | string | Folder path of the original workbook.                                                                                                                            |
| storageName               | string | Name of the storage where the source file is located.                                                                                                            |

## REST API

| API               | Type | Description                     | Swagger Link |
|-------------------|------|---------------------------------|--------------|
| /cells/{name}     | GET  | Exports a workbook to another format. | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project tasks. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}