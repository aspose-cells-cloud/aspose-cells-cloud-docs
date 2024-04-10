---
title: "Trendline"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/trendline/
description: "Aspose.Cells Cloud model specification : Trendline. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **trendline**

 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| link | Class:Link | True |  False |  |  |  
| Backward | Floating | True |  False |  | Returns or sets the number of periods (or units on a scatter chart) that the trendline extends backward.                         The number of periods must be greater than or equal to zero.                        If the chart type is column ,the number of periods must be between 0 and 0.5 |  
| DataLabels | Class:LinkElement | True |  False |  | Represents the DataLabels object for the specified series. |  
| DisplayEquation | Boolean | True |  False |  | Represents if the equation for the trendline is displayed on the chart (in the same data label as the R-squared value). Setting this property to True automatically turns on data labels. |  
| DisplayRSquared | Boolean | True |  False |  | Represents if the R-squared value of the trendline is displayed on the chart (in the same data label as the equation). Setting this property to True automatically turns on data labels. |  
| Forward | Floating | True |  False |  | Returns or sets the number of periods (or units on a scatter chart) that the trendline extends forward.                        The number of periods must be greater than or equal to zero. |  
| Intercept | Floating | True |  False |  | Returns or sets the point where the trendline crosses the value axis. |  
| IsNameAuto | Boolean | True |  False |  | Returns if Microsoft Excel automatically determines the name of the trendline. |  
| LegendEntry | Class:LinkElement | True |  False |  | Gets the legend entry according to this trendline |  
| Name | String | True |  False |  | Returns the name of the trendline. |  
| Order | Integer | True |  False |  | Returns or sets the trendline order (an integer greater than 1) when the trendline type is Polynomial.                         The order must be between 2 and 6. |  
| Period | Integer | True |  False |  | Returns or sets the period for the moving-average trendline. |  
| Type | String | True |  False |  | Returns the trendline type. |  
| BeginArrowLength | String | True |  False |  |  |  
| BeginArrowWidth | String | True |  False |  |  |  
| BeginType | String | True |  False |  |  |  
| CapType | String | True |  False |  |  |  
| Color | Class:Color | True |  False |  |  |  
| CompoundType | String | True |  False |  |  |  
| DashType | String | True |  False |  |  |  
| EndArrowLength | String | True |  False |  |  |  
| EndArrowWidth | String | True |  False |  |  |  
| EndType | String | True |  False |  |  |  
| GradientFill | Class:GradientFill | True |  False |  |  |  
| IsAuto | Boolean | True |  False |  |  |  
| IsAutomaticColor | Boolean | True |  False |  |  |  
| IsVisible | Boolean | True |  False |  |  |  
| JoinType | String | True |  False |  |  |  
| Style | String | True |  False |  |  |  
| Transparency | Floating | True |  False |  |  |  
| Weight | String | True |  False |  |  |  
| WeightPt | Floating | True |  False |  |  |  

**Parent Name** : (Line)[line]

