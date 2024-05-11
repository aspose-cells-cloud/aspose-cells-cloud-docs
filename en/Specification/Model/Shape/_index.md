---
title: "Shape"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/shape/
description: "Aspose.Cells Cloud model specification : Shape. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **shape**

Represents the msodrawing object. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Name | String | True |  False |  | Gets and sets the name of the shape. |  
| MsoDrawingType | String | True |  False |  | Gets mso drawing type. |  
| AutoShapeType | String | True |  False |  | Gets and sets the auto shape type. |  
| Placement | String | True |  False |  | Represents the way the drawing object is attached to the cells below it.                        The property controls the placement of an object on a worksheet. |  
| UpperLeftRow | Integer | True |  False |  | Represents upper left corner row index. |  
| Top | Integer | True |  False |  | Represents the vertical offset of shape from its top row, in unit of pixels. |  
| UpperLeftColumn | Integer | True |  False |  | Represents upper left corner column index. |  
| Left | Integer | True |  False |  | Represents the horizontal offset of shape from its left column, in unit of pixels. |  
| LowerRightRow | Integer | True |  False |  | Represents lower right corner row index. |  
| Bottom | Integer | True |  False |  | Represents the width of the shape's vertical offset from its lower bottom corner row, in unit of pixels. |  
| LowerRightColumn | Integer | True |  False |  | Represents lower right corner column index. |  
| Right | Integer | True |  False |  | Represents the width of the shape's horizontal  offset from its lower right corner column, in unit of pixels. |  
| Width | Integer | True |  False |  | Represents the width of shape, in unit of pixels. |  
| Height | Integer | True |  False |  | Represents the height of shape, in unit of pixel. |  
| X | Integer | True |  False |  | Gets and sets the horizontal offset of shape from worksheet left border,in unit of pixels. |  
| Y | Integer | True |  False |  | Gets and sets the vertical offset of shape from worksheet top border,in unit of pixels. |  
| RotationAngle | Floating | True |  False |  | Gets and sets the rotation of the shape. |  
| HtmlText | String | True |  False |  | Gets and sets the html string which contains data and some formats in this textbox. |  
| Text | String | True |  False |  | Represents the string in this TextBox object. |  
| AlternativeText | String | True |  False |  | Returns or sets the descriptive (alternative) text string of the  object. |  
| TextHorizontalAlignment | String | True |  False |  | Gets and sets the text horizontal alignment type of the shape. |  
| TextHorizontalOverflow | String | True |  False |  | Gets and sets the text horizontal overflow type of the shape which contains text. |  
| TextOrientationType | String | True |  False |  | Gets and sets the text orientation type of the shape. |  
| TextVerticalAlignment | String | True |  False |  | Gets and sets the text vertical alignment type of the shape. |  
| TextVerticalOverflow | String | True |  False |  | Gets and sets the text vertical overflow type of the shape which contains text. |  
| IsGroup | Boolean | True |  False |  | Indicates whether the shape is a group. |  
| IsHidden | Boolean | True |  False |  | Indicates whether the object is visible. |  
| IsLockAspectRatio | Boolean | True |  False |  | True means that don't allow changes in aspect ratio. |  
| IsLocked | Boolean | True |  False |  | True if the object is locked, False if the object can be modified when the sheet is protected. |  
| IsPrintable | Boolean | True |  False |  | True if the object is printable |  
| IsTextWrapped | Boolean | True |  False |  | Gets and sets the text wrapped type of the shape which contains text. |  
| IsWordArt | Boolean | True |  False |  | Indicates whether this shape is a word art. |  
| LinkedCell | String | True |  False |  | Gets or sets the worksheet range linked to the control's value. |  
| ZOrderPosition | Integer | True |  False |  | Returns the position of a shape in the z-order. |  
| Font | Class:Font | True |  False |  | Represents the font of shape. |  
| Hyperlink | String | True |  False |  | Gets the hyperlink of the shape. |  
| link | Class:Link | True |  False |  |  |  

**Parent Name** : [LinkElement](linkelement)

**Children Name** : 
	-  [ArcShape](arcshape) 
	-  [AutoShape](autoshape) 
	-  [Button](button) 
	-  [CellsDrawing](cellsdrawing) 
	-  [CheckBox](checkbox) 
	-  [ComboBox](combobox) 
	-  [CommentShape](commentshape) 
	-  [Form](form) 
	-  [GroupBox](groupbox) 
	-  [GroupShape](groupshape) 
	-  [Label](label) 
	-  [LineShape](lineshape) 
	-  [ListBox](listbox) 
	-  [OleObject](oleobject) 
	-  [Oval](oval) 
	-  [Picture](picture) 
	-  [RadioButton](radiobutton) 
	-  [RectangleShape](rectangleshape) 
	-  [ScrollBar](scrollbar) 
	-  [Spinner](spinner) 
	-  [TextBox](textbox) 
	-  [ChartShape](chartshape) 
