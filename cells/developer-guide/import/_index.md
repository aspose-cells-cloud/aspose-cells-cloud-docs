---
title: "Import"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: "Import data into Excel files."
description: "Aspose.Cells Cloud REST API support importing data into Excel files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."

weight: 31
---

Importing data into an Excel file is a complex process. Many factors contribute to the complexity and therefore, should be taken into account during the export process. The ability to imports kinds of formats and types of data into the file with a precise professional quality is a top feature of Aspose.Cells Cloud.

## RSET APIs

The following APIs to import data into an Excel file or multiple Excel files is provided:

|API|Description|
| :- | :- |
|[POST /cells/impport](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)| Import data into Excel files without using storage.|
|[POST /cells/{name}/impportdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Import data into the Excel file with using storage.|

## Request Parameters
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| file | file | formData | File to upload |
| ImportOption | ImportOptions | HTTPBody |  IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture |


The important parameters are described in the following table:

{{< tabs tabTotal="9" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntegerArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
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
{{< tab tabNum="5" >}}
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
{{< tab tabNum="6" >}}
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
{{< tab tabNum="7" >}}
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
{{< tab tabNum="8" >}}
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
{{< tab tabNum="9" >}}
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

The following articles explain each API how to call in detail and contain cURL and SDK Examples of each API:

- [How to import data into Excel files without using storage.](/cells/import/without-using-storage)
- [How to import data into Excel files with using storage.](/cells/import/with-using-storage)
- [How to import Batch Data into Excel Worksheet](/cells/import-batch-data-into-worksheet/)
- [How to import Double Array into Excel Worksheet](/cells/import-double-array-into-worksheet/)
- [How to import Integer Array into Excel Worksheet](/cells/import-integer-array-into-worksheet/)
- [How to import String Array into Excel Worksheet](/cells/import-string-array-into-worksheet/)
- [How to import CSV Data into Excel Worksheet](/cells/import-csv-data-into-worksheet/)
- [How to import 2 Dimension Double Array into Excel Worksheet](/cells/import-2dimension-double-array-into-worksheet/)
- [How to import 2 Dimension Integer Array into Excel Worksheet](/cells/import-2dimension-integer-array-into-worksheet/)
- [How to iImport 2 Dimension String Array into Excel Worksheet](/cells/import-2dimension-string-array-into-worksheet/)
