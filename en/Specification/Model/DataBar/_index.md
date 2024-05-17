---
title: "DataBar"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/databar/
description: "Aspose.Cells Cloud model specification : DataBar. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, DataBar
weight: 50
---

## **dataBar**

Describe the DataBar conditional formatting rule. This conditional formatting   rule displays a gradated data bar in the range of cells. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| AxisColor | Class:Color | True |  False |  | Gets the color of the axis for cells with conditional formatting as data bars.  |  
| AxisPosition | String | True |  False |  | Gets or sets the position of the axis of the data bars specified by a conditional formatting rule.  |  
| BarBorder | Class:DataBarBorder | True |  False |  | Gets an object that specifies the border of a data bar.  |  
| BarFillType | String | True |  False |  | Gets or sets how a data bar is filled with color.  |  
| Color | Class:Color | True |  False |  | Get or set this DataBar's Color.  |  
| Direction | String | True |  False |  | Gets or sets the direction the databar is displayed.  |  
| MaxCfvo | Class:ConditionalFormattingValue | True |  False |  | Get or set this DataBar's max value object.            Cannot set null or CFValueObject with type FormatConditionValueType.Min to it.  |  
| MaxLength | Integer | True |  False |  | Represents the max length of data bar .  |  
| MinCfvo | Class:ConditionalFormattingValue | True |  False |  | Get or set this DataBar's min value object.            Cannot set null or CFValueObject with type FormatConditionValueType.Max to it.  |  
| MinLength | Integer | True |  False |  | Represents the min length of data bar .  |  
| NegativeBarFormat | Class:NegativeBarFormat | True |  False |  | Gets the NegativeBarFormat object associated with a data bar conditional formatting rule.  |  
| ShowValue | Boolean | True |  False |  | Get or set the flag indicating whether to show the values of the cells on which this data bar is applied.            Default value is true.  |  

