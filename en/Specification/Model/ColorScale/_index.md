---
title: "ColorScale"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/colorscale/
description: "Aspose.Cells Cloud model specification : ColorScale. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, ColorScale
weight: 50
---

## **colorScale**

Describe the ColorScale conditional formatting rule. This conditional formatting   rule creates a gradated color scale on the cells.             

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| MaxCfvo | Class:ConditionalFormattingValue | True |  False |  | Get or set this ColorScale's max value object.            Cannot set null or CFValueObject with type FormatConditionValueType.Min to it.  |  
| MaxColor | Class:Color | True |  False |  | Get or set the gradient color for the maximum value in the range.  |  
| MidCfvo | Class:ConditionalFormattingValue | True |  False |  | Get or set this ColorScale's mid value object.            Cannot set CFValueObject with type FormatConditionValueType.Max or FormatConditionValueType.Min to it.  |  
| MidColor | Class:Color | True |  False |  | Get or set the gradient color for the middle value in the range.  |  
| MinCfvo | Class:ConditionalFormattingValue | True |  False |  | Get or set this ColorScale's min value object.            Cannot set null or CFValueObject with type FormatConditionValueType.Max to it.  |  
| MinColor | Class:Color | True |  False |  | Get or set the gradient color for the minimum value in the range.  |  

