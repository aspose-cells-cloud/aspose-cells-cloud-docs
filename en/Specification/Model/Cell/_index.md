---
title: "Cell"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/cell/
description: "Aspose.Cells Cloud model specification : Cell. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **cell**

Encapsulates the object that represents a single Workbook cell. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Name | String | True |  False |  | Gets the name of the cell. |  
| Row | Integer | True |  False |  | Gets row number (zero based) of the cell. |  
| Column | Integer | True |  False |  | Gets column number (zero based) of the cell. |  
| Value | String | True |  False |  | Gets the value contained in this cell. |  
| Type | String | True |  False |  | Represents cell value type. |  
| Formula | String | True |  False |  | Gets or sets a formula of the . |  
| IsFormula | Boolean | True |  False |  | Represents if the specified cell contains formula. |  
| IsMerged | Boolean | True |  False |  | Checks if a cell is part of a merged range or not. |  
| IsArrayHeader | Boolean | True |  False |  | Indicates the cell's formula is and array formula                         and it is the first cell of the array. |  
| IsInArray | Boolean | True |  False |  | Indicates whether the cell formula is an array formula. |  
| IsErrorValue | Boolean | True |  False |  | Checks if the value of this cell is an error. |  
| IsInTable | Boolean | True |  False |  | Indicates whether this cell is part of table formula. |  
| IsStyleSet | Boolean | True |  False |  | Indicates if the cell's style is set. If return false, it means this cell has a default cell format. |  
| HtmlString | String | True |  False |  | Gets and sets the html string which contains data and some formats in this cell. |  
| Style | Class:LinkElement | True |  False |  |  |  
| Worksheet | String | True |  False |  | Gets the parent worksheet. |  
| link | Class:Link | True |  False |  |  |  

**Parent Name** : [LinkElement](linkelement)

