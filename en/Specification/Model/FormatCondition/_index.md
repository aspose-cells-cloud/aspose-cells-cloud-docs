---
title: "FormatCondition"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/formatcondition/
description: "Aspose.Cells Cloud model specification : FormatCondition. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **formatCondition**

Represents conditional formatting condition. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Priority | Integer | True |  False |  | The priority of this conditional formatting rule. This value is used to determine which                        format should be evaluated and rendered. Lower numeric values are higher priority than                        higher numeric values, where '1' is the highest priority. |  
| Type | String | True |  False |  | Gets and sets whether the conditional format Type. |  
| StopIfTrue | Boolean | True |  False |  | True, no rules with lower priority may be applied over this rule, when this rule evaluates to true.                        Only applies for Excel 2007; |  
| AboveAverage | Class:AboveAverage | True |  False |  | Get the conditional formatting's "AboveAverage" instance.                        The default instance's rule highlights cells that are                         above the average for all values in the range.                        Valid only for type = AboveAverage. |  
| ColorScale | Class:ColorScale | True |  False |  | Get the conditional formatting's "ColorScale" instance.                        The default instance is a "green-yellow-red" 3ColorScale .                        Valid only for type = ColorScale. |  
| DataBar | Class:DataBar | True |  False |  | Get the conditional formatting's "DataBar" instance.                        The default instance's color is blue.                        Valid only for type is DataBar. |  
| Formula1 | String | True |  False |  | Gets and sets the value or expression associated with conditional formatting. |  
| Formula2 | String | True |  False |  | Gets and sets the value or expression associated with conditional formatting. |  
| IconSet | Class:IconSet | True |  False |  | Get the conditional formatting's "IconSet" instance.                        The default instance's IconSetType is TrafficLights31.                        Valid only for type = IconSet. |  
| Operator | String | True |  False |  | Gets and sets the conditional format operator type. |  
| Style | Class:Style | True |  False |  | Gets or setts style of conditional formatted cell ranges. |  
| Text | String | True |  False |  | The text value in a "text contains" conditional formatting rule.                         Valid only for type = containsText, notContainsText, beginsWith and endsWith.                        The default value is null. |  
| TimePeriod | String | True |  False |  | The applicable time period in a "date occurring…" conditional formatting rule.                         Valid only for type = timePeriod.                        The default value is TimePeriodType.Today. |  
| Top10 | Class:Top10 | True |  False |  | Get the conditional formatting's "Top10" instance.                        The default instance's rule highlights cells whose                        values fall in the top 10 bracket.                        Valid only for type is Top10. |  
| link | Class:Link | True |  False |  |  |  

**Parent Name** : [LinkElement](linkelement)

**Children Name** : 
	-  [StyleFormatCondition](styleformatcondition) 
