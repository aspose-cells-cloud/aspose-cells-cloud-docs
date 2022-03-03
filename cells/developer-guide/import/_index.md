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

The following APIs to import data into an Excel file or multiple Excel files is provided:

|API|Description|
| :- | :- |
|[POST /cells/impport](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)| Import data into Excel files without using storage.|
|[POST /cells/{name}/impportdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Import data into the Excel file with using storage.|


**The request parameters are:** 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| file | file | formData | File to upload |
| ImportOption | ImportOptions | HTTPBody |  IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture |

The important parameters are described in the following table:

- **Import2DimensionIntegerArrayOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FirstRow | int |  |
| FirstColumn | int |  |
| Data | Integer[,] |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | IntArray|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |


- **Import2DimensionDoubleArrayOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FirstRow | int |  |
| FirstColumn | int |  |
| Data | Double[,] |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | DoubleArray|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |

  
- **Import2DimensionStringArrayOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FirstRow | int |  |
| FirstColumn | int |  |
| Data | String[,] |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | StringArray|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |


- **ImportBatchDataOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| BatchData | List<CellValue> | batch data | 
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | BatchData|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |



- **CellValue**

| Parameter Name|Type|Description|
| :- | :- | :- |
| rowIndex | int |  | 
| columnIndex | int |  | 
| type | string | data type |
| value | string |  |
| style | Style(object) |  |


- **FileSource**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FileSourceType | string | InMemoryFiles/CloudFileSystem/RequestFiles | 
| FilePath | string | file position |


- **ImportCSVDataOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| SeparatorString | string |  |
| ConvertNumericData | string | true/false.|
| FirstRow | int | |
| FirstColumn | int | |
| SourceFile | string | |
| CustomParsers | List<CustomParserConfig> |  |


- **CustomParserConfig**

| Parameter Name|Type|Description|
| :- | :- | :- |
| ColumnIndex | int |  |
| ParseMethod | string |  |
| CustomStyle | string |  |

- **ImportDoubleArrayOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FirstRow | int |  |
| FirstColumn | int |  |
| IsVertical | string | true/false. |
| Data | Double[] |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | TwoDimensionDoubleArray|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |


- **ImportIntegerArrayOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FirstRow | int |  |
| FirstColumn | int |  |
| IsVertical | string | true/false. |
| Data | Integer[] |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | TwoDimensionIntArray|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |


- **ImportPictureOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| UpperLeftRow | int |  |
| UpperLeftColumn | int |  |
| LowerRightRow | int |  |
| LowerRightColumn | int |  |
| Filename | string | |
| Data | String |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | Picture |
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |

- **ImportStringArrayOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FirstRow | int |  |
| FirstColumn | int |  |
| IsVertical | string | true/false. |
| Data | String[] |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | TwoDimensionStringArray|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |
| DestinationWorksheet | string | destination work sheet name. |


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
