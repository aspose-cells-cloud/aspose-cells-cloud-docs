---
title: "Import Data into Excel files and Export data from Excel files."
second_title: "Aspose.Cells Cloud Document"
linktitle: "Import and Export Data"
type: docs
url: /data-import-and-export/
keywords: "Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction."
description: "Generate new documents or reports that can include charts, tables, and other data visualization elements"
weight: 25
kwords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction.
---

Aspose.Cells Cloud API supports importing data from a variety of data sources, and can export data from Excel, charts, and charts to different formats, including Excel, CSV, PDF, HTML, PNG, etc. This makes data management and sharing simple and efficient.

## How to import data from various data sources

Importing data into an Excel file is a complex process. Many factors contribute to the complexity and therefore, should be taken into account during the export process. The ability to imports kinds of formats and types of data into the file with a precise professional quality is a top feature of Aspose.Cells Cloud.

### Import Data APIs Information

The following APIs to import data into an Excel file or multiple Excel files is provided:

|API|Description|
| :- | :- |
|[POST /cells/impport](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)| Import data into Excel files without using storage.|
|[POST /cells/{name}/impportdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Import data into the Excel file with using storage.|

### Request Parameters

#### Without using storage

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| file | file | formData | File to upload |
| ImportOption | ImportOptions | HTTPBody |  IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture |

#### With using storage

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| name | string | path |   |
| folder | string | query |   |
| storageName | string | query | storage name. |
| importData |  | body |   |

#### Import data option parameter

**The important parameters are described in the following table**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>BatchData</td><td>List<CellValue></td> <td>batch data</td> </tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>ConvertNumericData</td><td>String</td> <td>true/false.</td> </tr>
    <tr> <td>FirstRow</td><td>int</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>int</td><td></td></tr>
    <tr><td>SeparatorString</td><td> String </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>CustomParsers</td><td>List<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>CSVData</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>int</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>int</td><td></td></tr>
    <tr><td>IsVertical</td><td>String</td><td>true/false.</td></tr>
    <tr><td>Data</td><td> String[] </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>Picture</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>int</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>int</td><td></td></tr>
    <tr><td>Data</td><td> Integer[,] </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>int</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>int</td><td></td></tr>
    <tr><td>Data</td><td> Double[,] </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>int</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>int</td><td></td></tr>
    <tr><td>Data</td><td> String[,] </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>int</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>int</td><td></td></tr>
    <tr><td>IsVertical</td><td>String</td><td>true/false.</td></tr>
    <tr><td>Data</td><td> Integer[] </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>IntegerArray</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>int</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>int</td><td></td></tr>
    <tr><td>IsVertical</td><td>String</td><td>true/false.</td></tr>
    <tr><td>Data</td><td> Double[] </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>DoubleArray</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr> <td>UpperLeftRow</td><td>int</td> <td></td> </tr>
    <tr> <td>UpperLeftColumn</td><td>int</td><td></td></tr>
    <tr> <td>LowerRightRow</td><td>int</td> <td></td> </tr>
    <tr> <td>LowerRightColumn</td><td>int</td><td></td></tr>
    <tr><td>Filename</td><td>String</td><td></td></tr>
    <tr><td>Data</td><td> String </td> <td></td></tr>
    <tr> <td>DestinationWorksheet</td><td> String </td><td> Destination work sheet name.</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>true/false.</td></tr>
    <tr><td>ImportDataType</td><td> String </td><td>StringArray</td></tr>
    <tr> <td>Source</td><td> FileSource </td><td>Indicates data file position when the BatchData parameter is null.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td> <td></td> </tr>
    <tr><td>columnIndex</td><td>int</td><td></td></tr>
    <tr><td>type</td><td>String</td><td>data type</td></tr>
    <tr><td>value</td><td>String </td> <td></td></tr>
    <tr><td>style</td><td> Style(object) </td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Type</th> <th scope="col">Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>String</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>FilePath</td><td>String</td><td> file position</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## How to export Excel objects to various file formats

If you have originally created an Excel file in a certain format, like [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), and [CSV](https://docs.fileformat.com/spreadsheet/csv/), you may sometimes find it useful to convert the excel file to another format so you can take advantage of special features provided by it. For example, you may want to export an excel file to [PDF](https://docs.fileformat.com/pdf/) to protect your contents from any unauthorized modifications and make it easy to read and share simultaneously.

Excel object export is a complex process. Many factors contribute to the complexity and therefore, should be taken into account during the export process. The ability to export Excel object to one format file with a precise professional quality is a top feature of Aspose.Cells Cloud.

It works perfectly for workbook, chart, shape and picture exported from excel file. You can export formats: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/). The export-only formats: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the data file and the second contains save options.

The REST API `export` workbook and internal objects to different format file.

### Export API Information

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

The request parameters are:

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| file | file | formData | File to upload |
| objectType | string | query |  object type (workbook/worksheet/chart/shape/picture/listobject/oleobject) |
| format | string | query | [File Format](/cells/supported-file-formats/)  |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

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

{{< /tab >}}

{{< /tabs >}}

## How to call import and export APIs

The following articles explain each API how to call in detail and contain cURL and SDK Examples of each API:

- [How to import data into Excel files without using storage.](/cells/import/without-using-storage)
- [How to import data into Excel files with using storage.](/cells/import/with-using-storage)
- [How to import Batch Data into Excel Worksheet](/cells/import-batch-data-into-excel-worksheet/)
- [How to import CSV Data into Excel Worksheet](/cells/import-csv-data-into-excel-worksheet/)
- [How to import picture into Excel Worksheet](/cells/import-picture-into-excel-worksheet/)
- [How to import Integer Array into Excel Worksheet](/cells/import-integer-array-into-excel-worksheet/)
- [How to import Double Array into Excel Worksheet](/cells/import-double-array-into-excel-worksheet/)
- [How to import String Array into Excel Worksheet](/cells/import-string-array-into-excel-worksheet/)
- [How to import 2 Dimension Integer Array into Excel Worksheet](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [How to import 2 Dimension Double Array into Excel Worksheet](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [How to import 2 Dimension String Array into Excel Worksheet](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Export Excel chart to different file format](/cells/export-excel-chart-to-different-formats/)
- [Export Excel list-object to different file format](/cells/export-excel-listobject-to-different-formats/)
- [Export Excel ole-object to different file format](/cells/export-excel-ole-object/)
- [Export Excel picture to different file format](/cells/export-excel-picture-to-different-formats/)
- [Export Excel shape to different file format](/cells/export-excel-shape-to-different-formats/)
- [Export Excel workbook to different file format](/cells/export-excel-to-different-formats/)
- [Export Excel worksheet to different file format](/cells/export-excel-worksheet-to-different-formats//)
