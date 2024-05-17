---
title: "Worksheet"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/worksheet/
description: "Aspose.Cells Cloud model specification : Worksheet. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, Worksheet
weight: 50
---

## **worksheet**

           Encapsulates the object that represents a single worksheet.            

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Links | Container | True |  False |  |  |  
| DisplayRightToLeft | Boolean | True |  False |  | Indicates if the specified worksheet is displayed from right to left instead of from left to right.            Default is false.  |  
| DisplayZeros | Boolean | True |  False |  | True if zero values are displayed.  |  
| FirstVisibleColumn | Integer | True |  False |  | Represents first visible column index.  |  
| FirstVisibleRow | Integer | True |  False |  | Represents first visible row index.  |  
| Name | String | True |  False |  | Gets or sets the name of the worksheet.  |  
| Index | Integer | True |  False |  | Gets the index of sheet in the worksheet collection.  |  
| IsGridlinesVisible | Boolean | True |  False |  | Gets or sets a value indicating whether the gridlines are visible.Default is true.  |  
| IsOutlineShown | Boolean | True |  False |  | Indicates whether to show outline.  |  
| IsPageBreakPreview | Boolean | True |  False |  | Indicates whether the specified worksheet is shown in normal view or page break preview.  |  
| IsVisible | Boolean | True |  False |  | Represents if the worksheet is visible.  |  
| IsProtected | Boolean | True |  False |  | Indicates if the worksheet is protected.  |  
| IsRowColumnHeadersVisible | Boolean | True |  False |  | Gets or sets a value indicating whether the worksheet will display row and column headers.            Default is true.  |  
| IsRulerVisible | Boolean | True |  False |  | Indicates whether the ruler is visible. This property is only applied for page break preview.  |  
| IsSelected | Boolean | True |  False |  | Indicates whether this worksheet is selected when the workbook is opened.  |  
| TabColor | Class:Color | True |  False |  | Represents worksheet tab color.  |  
| TransitionEntry | Boolean | True |  False |  | Indicates whether the Transition Formula Entry (Lotus compatibility) option is enabled.  |  
| TransitionEvaluation | Boolean | True |  False |  | Indicates whether the Transition Formula Evaluation (Lotus compatibility) option is enabled.  |  
| Type | String | True |  False |  | Represents worksheet type.  |  
| ViewType | String | True |  False |  | Gets and sets the view type.  |  
| VisibilityType | String | True |  False |  | Indicates the visible state for this sheet.  |  
| Zoom | Integer | True |  False |  | Represents the scaling factor in percentage. It should be between 10 and 400.  |  
| Cells | Class:LinkElement | True |  False |  | Gets the  collection.  |  
| Charts | Class:LinkElement | True |  False |  | Gets a  collection  |  
| AutoShapes | Class:LinkElement | True |  False |  |  |  
| OleObjects | Class:LinkElement | True |  False |  | Represents a collection of  in a worksheet.  |  
| Comments | Class:LinkElement | True |  False |  | Gets the  collection.  |  
| Pictures | Class:LinkElement | True |  False |  | Gets a  collection.  |  
| MergedCells | Class:LinkElement | True |  False |  |  |  
| Validations | Class:LinkElement | True |  False |  | Gets the data validation setting collection in the worksheet.  |  
| ConditionalFormattings | Class:LinkElement | True |  False |  | Gets the ConditionalFormattings in the worksheet.  |  
| Hyperlinks | Class:LinkElement | True |  False |  | Gets the  collection.  |  

