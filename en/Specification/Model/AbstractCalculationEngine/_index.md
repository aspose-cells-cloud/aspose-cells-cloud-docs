---
title: "AbstractCalculationEngine"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /abstractcalculationengine/
description: "Represents user's custom calculation engine to extend the default calculation engine of Aspose.Cells. "
weight: 50
---

## **abstractCalculationEngine**

Represents user's custom calculation engine to extend the default calculation engine of Aspose.Cells.  

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| IsParamLiteralRequired | Boolean | True |  False |  | Indicates whether this engine needs the literal text of parameter while doing calculation. Default value is false.  |  
| IsParamArrayModeRequired | Boolean | True |  False |  | Indicates whether this engine needs the parameter to be calculated in array mode. Default value is false.            If  is required when calculating custom            functions, this property needs to be set as true.  |  
| ProcessBuiltInFunctions | Boolean | True |  False |  | Whether built-in functions that have been supported by the built-in engine            should be checked and processed by this implementation.            Default is false.            If user needs to change the calculation logic of some built-in functions, this property should be set as true.            Otherwise please leave this property as false for performance consideration.  |  

