---
title: "Style"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/style/
description: ""
weight: 50
---

## **style**

 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Font | Class:Font | True |  False |  | Gets a  object.  |  
| Name | String | True |  False |  | Gets or sets the name of the style.  |  
| CultureCustom | String | True |  False |  | Gets and sets the culture-dependent pattern string for number format.            If no number format has been set for this object, null will be returned.            If number format is builtin, the pattern string corresponding to the builtin number will be returned.  |  
| Custom | String | True |  False |  | Represents the custom number format string of this style object.            If the custom number format is not set(For example, the number format is builtin), "" will be returned.  |  
| BackgroundColor | Class:Color | True |  False |  | Gets or sets a style's background color.  |  
| ForegroundColor | Class:Color | True |  False |  | Gets or sets a style's foreground color.  |  
| IsFormulaHidden | Boolean | True |  False |  | Represents if the formula will be hidden when the worksheet is protected.  |  
| IsDateTime | Boolean | True |  False |  | Indicates whether the number format is a date format.  |  
| IsTextWrapped | Boolean | True |  False |  | Gets or sets a value indicating whether the text within a cell is wrapped.  |  
| IsGradient | Boolean | True |  False |  | Indicates whether the cell shading is a gradient pattern.  |  
| IsLocked | Boolean | True |  False |  | Gets or sets a value indicating whether a cell can be modified or not.  |  
| IsPercent | Boolean | True |  False |  | Indicates whether the number format is a percent format.  |  
| ShrinkToFit | Boolean | True |  False |  | Represents if text automatically shrinks to fit in the available column width.  |  
| IndentLevel | Integer | True |  False |  | Represents the indent level for the cell or range. Can only be an integer from 0 to 250.  |  
| Number | Integer | True |  False |  | Gets or sets the display format of numbers and dates. The formatting patterns are different for different regions.  |  
| RotationAngle | Integer | True |  False |  | Represents text rotation angle.  |  
| Pattern | String | True |  False |  | Gets or sets the cell background pattern type.  |  
| TextDirection | String | True |  False |  | Represents text reading order.  |  
| VerticalAlignment | String | True |  False |  | Gets or sets the vertical alignment type of the text in a cell.  |  
| HorizontalAlignment | String | True |  False |  | Gets or sets the horizontal alignment type of the text in a cell.  |  
| BorderCollection | Container | True |  False |  |  |  
| BackgroundThemeColor | Class:ThemeColor | True |  False |  | Gets and sets the background theme color.  |  
| ForegroundThemeColor | Class:ThemeColor | True |  False |  | Gets and sets the foreground theme color.  |  

