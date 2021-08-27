---
title: "Get Cells Properties"
type: docs
url: /get-cells-properties/
weight: 130
---

This REST API indicates shows how to `get a specific cell` in an Excel file.

```bash

POST  http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}

```

- **Path Parameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| name | string |  The workbook name. |
| sheetName | string |  The worksheet name. |
| cellOrMethodName | string | value : firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn and cellName. |

- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|


- **Response**



{{< tabs tabTotal="2" tabID="1" tabName1="Response1" tabName2="Response2" >}}

{{< tab tabNum="1" >}}

```bash
{
    "Code": 200,
    "Status": "OK",
    "Cell":{
    }
}

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
    "StatusCode": 200,
    "Content": 'result_Content'
}

```

{{< /tab >}}

{{< /tabs >}}






- **Api Reference**   

 [GetWorksheetCell](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)



- **How to get specific cell**

   - [Get Cell Data from a Worksheet](/cells/get-cell-data-from-a-worksheet/)
   - [Get First Cell from Excel Worksheet](/cells/get-first-cell-from-excel-worksheet/)
   - [Get Last Cell of Excel Worksheet](/cells/get-last-cell-of-excel-worksheet/)
   - [Get MaxRow from Excel Worksheet](/cells/get-maxrow-from-excel-worksheet/)
   - [Get MaxDataRow from Excel Worksheet](/cells/get-maxdatarow-from-excel-worksheet/)
   - [Get MaxColumn from Excel Worksheet](/cells/get-maxcolumn-from-excel-worksheet/)
   - [Get MaxDataColumn from Excel Worksheet](/cells/get-maxdatacolumn-from-excel-worksheet/)
   - [Get MinRow from Excel Worksheet](/cells/get-minrow-from-excel-worksheet/)
   - [Get MinDataRow from Excel Worksheet](/cells/get-mindatarow-from-excel-worksheet/)
   - [Get MinColumn from Excel Worksheet](/cells/get-mincolumn-from-excel-worksheet/)
   - [Get MinDataColumn from Excel Worksheet](/cells/get-mindatacolumn-from-excel-worksheet/)
