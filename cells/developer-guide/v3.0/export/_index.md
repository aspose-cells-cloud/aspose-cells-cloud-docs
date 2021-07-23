---
title: "Export"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /export/
keywords: "REST API, convert, spreadsheets, excel"
description: "Cells.Cloud API for Excel export: export excel file or object in excel file to other format file."
weight: 100
---

If you have originally created an Excel file in a certain format, like [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), and [CSV](https://docs.fileformat.com/spreadsheet/csv/), you may sometimes find it useful to convert the excel file to another format so you can take advantage of special features provided by it. For example, you may want to export an excel file to [PDF](https://docs.fileformat.com/pdf/) to protect your contents from any unauthorized modifications and make it easy to read and share simultaneously. 

Excel object export is a complex process. Many factors contribute to the complexity and therefore, should be taken into account during the export process. The ability to export Excel object to one format file with a precise professional quality is a top feature of Aspose.Cells Cloud. 

It works perfectly for workbook, chart, shape and picture exported from excel file. You can export formats: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/). The export-only formats: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

This REST API `export` excel file to different format file.
```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the data file and the second contains save options.

- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|objectType |string | object type (workbook/chart/shape/picture)) |
|format|string| file format(csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg) |


- **Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|excel file|data file | The data file save into the first part of the multipart content.|

- **Response**

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
```

- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-LiteCells-Export.php" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "LiteCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


The following articles explain each API in detail and contain cURL and SDK Examples of each API:


1. [Export Excel chart to different file format](/cells/export/excel-chart-to-different-formats/)
2. [Export Excel picture to different file format](/cells/export/excel-picture-to-different-formats/)
3. [Export Excel shape to different file format](/cells/export/excel-shape-to-different-formats/)
4. [Export Excel workbook to different file format](/cells/export/excel-to-different-formats/)

