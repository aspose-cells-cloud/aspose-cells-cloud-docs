---
title: "AnalyzedTableDescription"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/analyzedtabledescription/
description: "Aspose.Cells Cloud model specification : AnalyzedTableDescription. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **analyzedTableDescription**

Represents analyzed table description. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Name | String | True |  False |  | Represents table name. |  
| SheetName | String | True |  False |  | Represents worksheet name which is where the table is located. |  
| Columns | Container | True |  False |  | Represents analyzed description about table columns. |  
| DateColumns | Container | True |  False |  | Represents date columns list. |  
| NumberColumns | Container | True |  False |  | Represents number columns list. |  
| TextColumns | Container | True |  False |  | Represents string columns list. |  
| ExceptionColumns | Container | True |  False |  | Represents exception columns list. |  
| HasTableHeaderRow | Boolean | True |  False |  | Represents there is a table header in the table. |  
| HasTableTotalRow | Boolean | True |  False |  | Represents there is a total row in the table. |  
| StartDataColumnIndex | Integer | True |  False |  | Represents the column index as the start data column. |  
| EndDataColumnIndex | Integer | True |  False |  | Represents the column index as the end data column. |  
| StartDataRowIndex | Integer | True |  False |  | Represents the row index as the start data row. |  
| EndDataRowIndex | Integer | True |  False |  | Represents the row index as the end data row. |  
| Thumbnail | String | True |  False |  | Represents table thumbnail. Base64String |  
| DiscoverCharts | Container | True |  False |  | Represents a collection of charts, which is a collection of charts created based on data analysis of a table. |  
| DiscoverPivotTables | Container | True |  False |  | Represents a collection of pivot tables, which is a collection of pivot tables created based on data analysis of a table. |  

