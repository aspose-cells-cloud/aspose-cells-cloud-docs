---
title: "WorkbookSettings"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/workbooksettings/
description: "Aspose.Cells Cloud model specification : WorkbookSettings. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **workbookSettings**

 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| AutoCompressPictures | Boolean | True |  False |  | Specifies a boolean value that indicates the application automatically compressed pictures in the workbook.  |  
| AutoRecover | Boolean | True |  False |  | Indicates whether the file is mark for auto-recovery.  |  
| BuildVersion | String | True |  False |  | Specifies the incremental public release of the application.  |  
| CalcMode | String | True |  False |  | It specifies whether to calculate formulas manually,            automatically or automatically except for multiple table operations.  |  
| CalculationId | String | True |  False |  | Specifies the version of the calculation engine used to calculate values in the workbook.  |  
| CheckComptiliblity | Boolean | True |  False |  | Indicates whether check comptiliblity when saving workbook.                         Remarks: The default value is true.              |  
| CheckExcelRestriction | Boolean | True |  False |  | Whether check restriction of excel file when user modify cells related objects.            For example, excel does not allow inputting string value longer than 32K.            When you input a value longer than 32K such as by Cell.PutValue(string), if this property is true, you will get an Exception.            If this property is false, we will accept your input string value as the cell's value so that later            you can output the complete string value for other file formats such as CSV.            However, if you have set such kind of value that is invalid for excel file format,            you should not save the workbook as excel file format later. Otherwise there may be unexpected error for the generated excel file.  |  
| CrashSave | Boolean | True |  False |  | indicates whether the application last saved the workbook file after a crash.  |  
| CreateCalcChain | Boolean | True |  False |  | Whether creates calculated formulas chain. Default is false.  |  
| DataExtractLoad | Boolean | True |  False |  | indicates whether the application last opened the workbook for data recovery.  |  
| Date1904 | Boolean | True |  False |  | Gets or sets a value which represents if the workbook uses the 1904 date system.  |  
| DisplayDrawingObjects | String | True |  False |  | Indicates whether and how to show objects in the workbook.  |  
| EnableMacros | Boolean | True |  False |  | Enable macros;  |  
| FirstVisibleTab | Integer | True |  False |  | Gets or sets the first visible worksheet tab.  |  
| HidePivotFieldList | Boolean | True |  False |  | Gets and sets whether hide the field list for the PivotTable.  |  
| IsDefaultEncrypted | Boolean | True |  False |  | Indicates whether encrypting the workbook with default password if Structure and Windows of the workbook are locked.  |  
| IsHidden | Boolean | True |  False |  | Indicates whether this workbook is hidden.  |  
| IsHScrollBarVisible | Boolean | True |  False |  | Gets or sets a value indicating whether the generated spreadsheet will contain a horizontal scroll bar.  |  
| IsMinimized | Boolean | True |  False |  | Represents whether the generated spreadsheet will be opened Minimized.  |  
| IsVScrollBarVisible | Boolean | True |  False |  | Gets or sets a value indicating whether the generated spreadsheet will contain a vertical scroll bar.  |  
| Iteration | Boolean | True |  False |  | Indicates whether enable iterative calculation to resolve circular references.  |  
| LanguageCode | String | True |  False |  | Gets or sets the user interface language of the Workbook version based on CountryCode that has saved the file.  |  
| MaxChange | Floating | True |  False |  | Returns or sets the maximum number of change to resolve a circular reference.  |  
| MaxIteration | Integer | True |  False |  | Returns or sets the maximum number of iterations to resolve a circular reference.  |  
| MemorySetting | String | True |  False |  | Gets or sets the memory usage options. The new option will be taken as the default option for newly created worksheets but does not take effect for existing worksheets.  |  
| NumberDecimalSeparator | String | True |  False |  | Gets or sets the decimal separator for formatting/parsing numeric values. Default is the decimal separator of current Region.  |  
| NumberGroupSeparator | String | True |  False |  | Gets or sets the character that separates groups of digits to the left of the decimal in numeric values. Default is the group separator of current Region.  |  
| ParsingFormulaOnOpen | Boolean | True |  False |  | Indicates whether parsing the formula when reading the file.  |  
| PrecisionAsDisplayed | Boolean | True |  False |  | True if calculations in this workbook will be done using only the precision of the numbers as they're displayed  |  
| RecalculateBeforeSave | Boolean | True |  False |  | Indicates whether to recalculate before saving the document.  |  
| ReCalculateOnOpen | Boolean | True |  False |  | Indicates whether re-calculate all formulas on opening file.  |  
| RecommendReadOnly | Boolean | True |  False |  | Indicates if the Read Only Recommended option is selected.             |  
| Region | String | True |  False |  | Gets or sets the regional settings for workbook.  |  
| RemovePersonalInformation | Boolean | True |  False |  | True if personal information can be removed from the specified workbook.  |  
| RepairLoad | Boolean | True |  False |  | Indicates whether the application last opened the workbook in safe or repair mode.  |  
| Shared | Boolean | True |  False |  | Gets or sets a value that indicates whether the Workbook is shared.  |  
| SheetTabBarWidth | Integer | True |  False |  | Width of worksheet tab bar (in 1/1000 of window width).  |  
| ShowTabs | Boolean | True |  False |  | Get or sets a value whether the Workbook tabs are displayed.  |  
| UpdateAdjacentCellsBorder | Boolean | True |  False |  | Indicates whether update adjacent cells' border.  |  
| UpdateLinksType | String | True |  False |  | Gets and sets how updates external links when the workbook is opened.  |  
| WindowHeight | Floating | True |  False |  | The height of the window, in unit of point.  |  
| WindowLeft | Floating | True |  False |  | The distance from the left edge of the client area to the left edge of the window, in unit of point.  |  
| WindowTop | Floating | True |  False |  | The distance from the top edge of the client area to the top edge of the window, in unit of point.  |  
| WindowWidth | Floating | True |  False |  | The width of the window, in unit of point.  |  
| Author | String | True |  False |  | Gets and sets the author of the file.  |  
| CheckCustomNumberFormat | Boolean | True |  False |  | Indicates whether checking custom number format when setting Style.Custom.  |  
| ProtectionType | String | True |  False |  | Gets the protection type of the workbook.  |  
| GlobalizationSettings | Class:GlobalizationSettings | True |  False |  | Gets and sets the globalization settings.  |  
| Password | String | True |  False |  | Represents Workbook file encryption password.  |  
| WriteProtection | Class:WriteProtection | True |  False |  | Provides access to the workbook write protection options.  |  
| IsEncrypted | Boolean | True |  False |  | Gets a value that indicates whether a password is required to open this workbook.  |  
| IsProtected | Boolean | True |  False |  | Gets a value that indicates whether the structure or window of the Workbook is protected.  |  
| MaxRow | Integer | True |  False |  | Gets the max row index, zero-based.  |  
| MaxColumn | Integer | True |  False |  | Gets the max column index, zero-based.  |  
| SignificantDigits | Integer | True |  False |  | Gets and sets the number of significant digits.            The default value is .  |  
| CheckCompatibility | Boolean | True |  False |  | Indicates whether check compatibility with earlier versions when saving workbook.  |  
| PaperSize | String | True |  False |  | Gets and sets the default print paper size.  |  
| MaxRowsOfSharedFormula | Integer | True |  False |  | Gets and sets the max row number of shared formula.  |  
| Compliance | String | True |  False |  | Specifies the OOXML version for the output document. The default value is Ecma376_2006.  |  
| QuotePrefixToStyle | Boolean | True |  False |  | Indicates whether setting  property when entering the string value(which starts  with single quote mark ) to the cell  |  
| FormulaSettings | Class:FormulaSettings | True |  False |  | Gets the settings for formula-related features.  |  
| ForceFullCalculate | Boolean | True |  False |  | Fully calculates every time when a calculation is triggered.  |  

