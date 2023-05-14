---
title: Get Cells Propertie
type: docs
url: /ar/get-cells-properties/
weight: 130
---
This REST API indicates shows how to `get a specific cell` in an Excel file.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
The request parameters are: 
 
|Parameter Name |Type |Path/Query String/HTTPBody |Description|
|:- |:- |:- |:- |
|name |string |path |Document name. |
|sheetName |string |path |Worksheet name. |
|cellOrMethodName |string |path |The cell's or method name. (Method name value : firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn and cellName.) |
|folder |string |query |Document's folder. |
|storageName |string |query |storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.


- **How to get specific cell**

   - [Get Cell Data from a Worksheet](/cells/ar/get-cell-data-from-a-worksheet/)
   - [Get First Cell from Excel Worksheet](/cells/ar/get-first-cell-from-excel-worksheet/)
   - [Get Last Cell of Excel Worksheet](/cells/ar/get-last-cell-of-excel-worksheet/)
   - [Get MaxRow from Excel Worksheet](/cells/ar/get-maxrow-from-excel-worksheet/)
   - [Get MaxDataRow from Excel Worksheet](/cells/ar/get-maxdatarow-from-excel-worksheet/)
   - [Get MaxColumn from Excel Worksheet](/cells/ar/get-maxcolumn-from-excel-worksheet/)
   - [Get MaxDataColumn from Excel Worksheet](/cells/ar/get-maxdatacolumn-from-excel-worksheet/)
   - [Get MinRow from Excel Worksheet](/cells/ar/get-minrow-from-excel-worksheet/)
   - [Get MinDataRow from Excel Worksheet](/cells/ar/get-mindatarow-from-excel-worksheet/)
   - [Get MinColumn from Excel Worksheet](/cells/ar/get-mincolumn-from-excel-worksheet/)
   - [Get MinDataColumn from Excel Worksheet](/cells/ar/get-mindatacolumn-from-excel-worksheet/)
