---
title: "Import"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: "REST API,  spreadsheets, excel, Import."
description: "Cells.Cloud API for Excel files import."
weight: 100
---

This REST API indicates `import data` in an Excel file.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import

```

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


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LiteCells/PostImport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/import" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
-F 'ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}'
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
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
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}

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

{{< /tab >}}

{{< /tabs >}}
