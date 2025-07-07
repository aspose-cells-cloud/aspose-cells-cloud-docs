---
title: "Excel to TIFF"
second_title: "Aspose.Cells Cloud Document"
linketitle: "Excel to Tiff"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/,/convert/excel-to-tiff/]
keywords: "Convert excel files to tiff files."
description: "Aspose.Cells Cloud REST API support conversion excel files to tiff files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 90
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Excel to TIFF
---

This REST API `saveas` excel file to TIFF.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API lets you save MS Excel file as TIFF file with additional settings and save the result to the storage.

This REST API `convert` excel file to TIFF.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API lets you convert MS Excel file to TIFF file with additional settings and save the result to the response.

This REST API `export` excel file to TIFF.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API lets you convert MS Excel file to TIFF file with additional settings and save the result to the response.

## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/convert|PUT|Converts workbook from request content to some format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/cells/{name}|GET|Exports workbook to other format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{name}/saveAs|POST|Export workbook to Format|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

These APIs define a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
-X POST \
-d "{'SaveFormat':'tiff', 'ImageFormat': 'tiff'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'tiff', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}
{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}
