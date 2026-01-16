---
title: "Import Data into Excel files and Export data from Excel files."
second_title: "Document"
linktitle: "Import and Export Data"
type: docs
url: /data-import-and-export/
keywords: "Excel data import, direct database access, batch data import, row-by-row data writing, automated data export, manual data extraction, Aspose.Cells Cloud API"
description: "Use Aspose.Cells Cloud API to import data from various sources into Excel files and export Excel workbooks, charts, and other objects to multiple formats such as XLSX, CSV, PDF, PNG, and more."
weight: 25
---

Aspose.Cells Cloud API supports importing data from a variety of sources and can export Excel workbooks, charts, and other objects to different formats, including XLSX, CSV, PDF, HTML, PNG, and more. This makes data management and sharing simple and efficient.

## How to import data from various data sources

Importing data into an Excel file is a complex process. Many factors contribute to the complexity and therefore should be taken into account during the import process. The ability to import many formats and types of data with professional quality is a top feature of Aspose.Cells Cloud.

### Import Data APIs Information

The following APIs are provided to import data into one or multiple Excel files:

| API | Description |
| :- | :- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) | Import data into Excel files without using storage. |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Import data into an Excel file stored in the cloud. |

### Request Parameters

#### Without using storage

| Parameter Name | Type | Location | Description |
| :- | :- | :- | :- |
| file | file | formData | File to upload |
| ImportOption | ImportOptions | HTTP body | Specifies the import format (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### With using storage

| Parameter Name | Type | Location | Description |
| :- | :- | :- | :- |
| name | string | path | Name of the Excel file |
| folder | string | query | Folder path in storage |
| storageName | string | query | Storage name |
| importData | ImportOptions | body | Import data payload |

#### Import data option parameters

**The important parameters are described in the following tables:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>Batch data to import</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>String</td><td>Whether to convert numeric data (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>Index of the first row</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index of the first column</td></tr>
    <tr><td>SeparatorString</td><td>String</td><td>Column separator</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Custom parser configurations</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index of the first row</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index of the first column</td></tr>
    <tr><td>IsVertical</td><td>String</td><td>Whether the picture is placed vertically (true/false)</td></tr>
    <tr><td>Data</td><td>String[]</td><td>Picture data (base‑64 strings)</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index of the first row</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index of the first column</td></tr>
    <tr><td>Data</td><td>Integer[,] </td><td>Two‑dimensional integer array</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index of the first row</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index of the first column</td></tr>
    <tr><td>Data</td><td>Double[,] </td><td>Two‑dimensional double array</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index of the first row</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index of the first column</td></tr>
    <tr><td>Data</td><td>String[,] </td><td>Two‑dimensional string array</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index of the first row</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index of the first column</td></tr>
    <tr><td>IsVertical</td><td>String</td><td>Whether the array is vertical (true/false)</td></tr>
    <tr><td>Data</td><td>Integer[] </td><td>One‑dimensional integer array</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index of the first row</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index of the first column</td></tr>
    <tr><td>IsVertical</td><td>String</td><td>Whether the array is vertical (true/false)</td></tr>
    <tr><td>Data</td><td>Double[] </td><td>One‑dimensional double array</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Upper‑left row index</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Upper‑left column index</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>Lower‑right row index</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Lower‑right column index</td></tr>
    <tr><td>Filename</td><td>String</td><td>Name of the source file</td></tr>
    <tr><td>Data</td><td>String</td><td>String data to import</td></tr>
    <tr><td>DestinationWorksheet</td><td>String</td><td>Destination worksheet name</td></tr>
    <tr><td>IsInsert</td><td>String</td><td>Whether to insert data (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>String</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Data file location when BatchData is null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Row index of the cell</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Column index of the cell</td></tr>
    <tr><td>type</td><td>String</td><td>Data type of the cell value</td></tr>
    <tr><td>value</td><td>String</td><td>Cell value</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>Cell style definition</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>String</td><td>InMemoryFiles, CloudFileSystem, or RequestFiles</td></tr>
    <tr><td>FilePath</td><td>String</td><td>Path to the source file</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## How to export Excel objects to various file formats

If you originally created an Excel file in a format such as **XLS**, **XLSX**, **XLSB**, or **CSV**, you may want to convert it to another format to take advantage of specific features. For example, exporting to **PDF** protects the content from unauthorized modifications while making it easy to read and share.

Exporting Excel objects is a complex process, and many factors must be considered. Aspose.Cells Cloud provides high‑quality export of workbooks, charts, shapes, and pictures to a wide range of formats:

*Export‑only formats*: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
*Both import and export*: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

The request uses multipart content as defined in [RFC 2046] and [RFC 1341]. The first part contains the data file; the second part contains save options.

### Export API Information

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### Request parameters

| Parameter Name | Type | Location | Description |
| :- | :- | :- | :- |
| file | file | formData | File to upload |
| objectType | string | query | Object type (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format | string | query | Desired output file format (see [Supported File Formats](/cells/supported-file-formats/)) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) defines a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to call the API. The example below demonstrates a request and its JSON response.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## How to call import and export APIs

The following articles explain each API in detail and contain cURL and SDK examples:

- [How to import data into Excel files without using storage.](/cells/import/without-using-storage)  
- [How to import data into Excel files with using storage.](/cells/import/with-using-storage)  
- [How to import Batch Data into Excel Worksheet](/cells/import-batch-data-into-excel-worksheet/)  
- [How to import CSV Data into Excel Worksheet](/cells/import-CSV-data-into-excel-worksheet/)  
- [How to import picture into Excel Worksheet](/cells/import-picture-into-excel-worksheet/)  
- [How to import Integer Array into Excel Worksheet](/cells/import-integer-array-into-excel-worksheet/)  
- [How to import Double Array into Excel Worksheet](/cells/import-double-array-into-excel-worksheet/)  
- [How to import String Array into Excel Worksheet](/cells/import-string-array-into-excel-worksheet/)  
- [How to import 2 Dimension Integer Array into Excel Worksheet](/cells/import-a-2D-integer-array-into-excel-worksheet/)  
- [How to import 2 Dimension Double Array into Excel Worksheet](/cells/import-a-2D-double-array-into-excel-worksheet/)  
- [How to import 2 Dimension String Array into Excel Worksheet](/cells/import-a-2D-string-array-into-excel-worksheet/)  
- [Export Excel chart to different file format](/cells/export-excel-chart-to-different-formats/)  
- [Export Excel list‑object to different file format](/cells/export-excel-listobject-to-different-formats/)  
- [Export Excel ole‑object to different file format](/cells/export-excel-ole-object/)  
- [Export Excel picture to different file format](/cells/export-excel-picture-to-different-formats/)  
- [Export Excel shape to different file format](/cells/export-excel-shape-to-different-formats/)  
- [Export Excel workbook to different file format](/cells/export-excel-to-different-formats/)  
- [Export Excel worksheet to different file format](/cells/export-excel-worksheet-to-different-formats/)