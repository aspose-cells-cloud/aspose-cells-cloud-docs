---
title: "CreatePivotTableRequest"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/createpivottablerequest/
description: "Indicates create pivot table request"
weight: 50
---

## **createPivotTableRequest**

Indicates create pivot table request 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Name | String | True |  False |  | Pivot table name |  
| SourceData | String | True |  False |  | The data for the new PivotTable cache. |  
| DestCellName | String | True |  False |  | The cell in the upper-left corner of the PivotTable report's destination range. |  
| UseSameSource | Boolean | True |  False |  | Indicates whether using same data source when another existing pivot table has used this data source.If the property is true, it will save memory. |  
| PivotFieldRows | Array<Integer> | True |  False |  | Represents row fields in a PivotTable report. |  
| PivotFieldColumns | Array<Integer> | True |  False |  | Represents column fields in a PivotTable report. |  
| PivotFieldData | Array<Integer> | True |  False |  | Represents data fields in a PivotTable report. |  

