---
title: "CalculationOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/calculationoptions/
description: "Aspose.Cells Cloud model specification : CalculationOptions. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **calculationOptions**

 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| CalcStackSize | Integer | True |  False |  | Specifies the stack size for calculating cells recursively.  |  
| IgnoreError | Boolean | True |  False |  | Indicates whether errors encountered while calculating formulas should be ignored.            The error may be unsupported function, external links, etc.            The default value is true.  |  
| PrecisionStrategy | String | True |  False |  | Specifies the strategy for processing precision of calculation.  |  
| Recursive | Boolean | True |  False |  | Indicates whether calculate the dependent cells recursively when calculating one cell and it depends on other cells.            The default value is true.  |  
| CustomEngine | Class:AbstractCalculationEngine | True |  False |  | The custom formula calculation engine to extend the default calculation engine of Aspose.Cells.  |  
| CalculationMonitor | Class:AbstractCalculationMonitor | True |  False |  | The monitor for user to track the progress of formula calculation.  |  
| LinkedDataSources | Array<Class:Workbook> | True |  False |  | Specifies the data sources for external links used in formulas.  |  

