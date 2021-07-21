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

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the data file and the second contains save options.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|objectType |string | object type (workbook/chart/shape/picture)) |
|format|string| file format(csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg) |


**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|excel file|data file | The data file save into the first part of the multipart content.|

**Response**

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
The following articles explain each API in detail and contain cURL and SDK Examples of each API:


- [Export Excel chart to different file format](/cells/export/excel-chart-to-different-formats/)
- [Export Excel picture to different file format](/cells/export/excel-picture-to-different-formats/)
- [Export Excel shape to different file format](/cells/export/excel-shape-to-different-formats/)
- [Export Excel workbook to different file format](/cells/export/excel-to-different-formats/)
