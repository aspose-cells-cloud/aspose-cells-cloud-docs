---
title: "AboveAverage"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/aboveaverage/
description: "Aspose.Cells Cloud model specification : AboveAverage. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, AboveAverage
weight: 50
---

## **aboveAverage**

Describe the AboveAverage conditional formatting rule. This conditional formatting    rule highlights cells that are above or below the average for all values    in the range. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| IsAboveAverage | Boolean | True |  False |  | Get or set the flag indicating whether the rule is an "above average" rule.             'true' indicates 'above average'.            Default value is true.  |  
| IsEqualAverage | Boolean | True |  False |  | Get or set the flag indicating whether the 'aboveAverage' and 'belowAverage' criteria             is inclusive of the average itself, or exclusive of that value.             'true' indicates to include the average value in the criteria.            Default value is false.  |  
| StdDev | Integer | True |  False |  | Get or set the number of standard deviations to include above or below the average in the            conditional formatting rule.             The input value must between 0 and 3 (include 0 and 3).             Setting this value to 0 means stdDev is not set.            The default value is 0.  |  

