---
title: "CopyOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/copyoptions/
description: "Aspose.Cells Cloud model specification : CopyOptions. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **copyOptions**

Represents the copy options. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| ColumnCharacterWidth | Boolean | True |  False |  | Indicates whether copying column width in unit of characters.  |  
| CopyInvalidFormulasAsValues | Boolean | True |  False |  | If the formula is not valid for the dest destination, only copy values.  |  
| CopyNames | Boolean | True |  False |  | Indicates whether copying the names.  |  
| ExtendToAdjacentRange | Boolean | True |  False |  | Indicates whether extend ranges when copying the range to adjacent range.  |  
| ReferToDestinationSheet | Boolean | True |  False |  | When copying the range in the same file and the chart refers to the source sheet,            False means the copied chart's data source will not be changed.            True means the copied chart's data source refers to the destination sheet.  |  
| ReferToSheetWithSameName | Boolean | True |  False |  | In ms excel, when copying formulas which refer to other worksheets while copying a worksheet to another one,            the copied formulas should refer to source workbook.            However, for some situations user may need the copied formulas refer to worksheets with the same name            in the same workbook, such as when those worksheets have been copied before this copy operation,            then this property should be kept as true.  |  

