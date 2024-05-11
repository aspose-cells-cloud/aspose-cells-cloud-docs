---
title: "Series"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/series/
description: "Aspose.Cells Cloud model specification : Series. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **series**

Encapsulates the object that represents a single data series in a chart. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Area | Class:Area | True |  False |  | Represents the background area of Series object. |  
| Bar3DShapeType | String | True |  False |  | Gets or sets the 3D shape type used with the 3-D bar or column chart. |  
| Border | Class:Line | True |  False |  | Represents border of Series object. |  
| BubbleScale | Integer | True |  False |  | Gets or sets the scale factor for bubbles in the specified chart group.                         It can be an integer value from 0 (zero) to 300,                         corresponding to a percentage of the default size.                        Applies only to bubble charts. |  
| BubbleSizes | String | True |  False |  | Gets or sets the bubble sizes values of the chart series. |  
| CountOfDataValues | Integer | True |  False |  | Gets the number of the data values. |  
| DataLabels | Class:LinkElement | True |  False |  | Represents the DataLabels object for the specified ASeries. |  
| DisplayName | String | True |  False |  | Gets the series's name that displays on the chart graph. |  
| DoughnutHoleSize | Integer | True |  False |  | Returns or sets the size of the hole in a doughnut chart group.                         The hole size is expressed as a percentage of the chart size, between 10 and 90 percent. |  
| DownBars | Class:LinkElement | True |  False |  | Returns a  object that represents the down bars on a line chart.                        Applies only to line charts. |  
| DropLines | Class:Line | True |  False |  | Returns a  object that represents the drop lines for a series on the line chart or area chart.                        Applies only to line chart or area charts. |  
| Explosion | Integer | True |  False |  | The distance of an open pie slice from the center of the pie chart is expressed as a percentage of the pie diameter. |  
| FirstSliceAngle | Integer | True |  False |  | Gets or sets the angle of the first pie-chart or doughnut-chart slice, in degrees (clockwise from vertical).                         Applies only to pie, 3-D pie, and doughnut charts, 0 to 360. |  
| GapWidth | Integer | True |  False |  | Returns or sets the space between bar or column clusters, as a percentage of the bar or column width.                        The value of this property must be between 0 and 500. |  
| Has3DEffect | Boolean | True |  False |  | True if the series has a three-dimensional appearance.                         Applies only to bubble charts. |  
| HasDropLines | Boolean | True |  False |  | True if the chart has drop lines.                        Applies only to line chart or area charts. |  
| HasHiLoLines | Boolean | True |  False |  | True if the line chart has high-low lines.                          Applies only to line charts. |  
| HasLeaderLines | Boolean | True |  False |  | True if the series has leader lines. |  
| HasRadarAxisLabels | Boolean | True |  False |  | True if a radar chart has category axis labels. Applies only to radar charts. |  
| HasSeriesLines | Boolean | True |  False |  | True if a stacked column chart or bar chart has series lines or                        if a Pie of Pie chart or Bar of Pie chart has connector lines between the two sections.                         Applies only to stacked column charts, bar charts, Pie of Pie charts, or Bar of Pie charts. |  
| HasUpDownBars | Boolean | True |  False |  | True if a line chart has up and down bars.                        Applies only to line charts. |  
| HiLoLines | Class:Line | True |  False |  | Returns a HiLoLines object that represents the high-low lines for a series on a line chart.                         Applies only to line charts. |  
| IsAutoSplit | Boolean | True |  False |  | Indicates whether the threshold value is automatic. |  
| IsColorVaried | Boolean | True |  False |  | Represents if the color of points is varied.                         The chart must contain only one series. |  
| LeaderLines | Class:Line | True |  False |  | Represents leader lines on a chart. Leader lines connect data labels to data points.                         This object isn’t a collection; there’s no object that represents a single leader line. |  
| LegendEntry | Class:LinkElement | True |  False |  | Gets the legend entry according to this series. |  
| Line | Class:Line | True |  False |  |  |  
| Marker | Class:Marker | True |  False |  | Gets the marker. |  
| Name | String | True |  False |  | Gets or sets the name of the data series. |  
| Overlap | Integer | True |  False |  | Specifies how bars and columns are positioned.                        Can be a value between – 100 and 100.                         Applies only to 2-D bar and 2-D column charts. |  
| PlotOnSecondAxis | Boolean | True |  False |  | Indicates if this series is plotted on second value axis. |  
| Points | Class:LinkElement | True |  False |  | Gets the collection of points in a series in a chart. |  
| SecondPlotSize | Integer | True |  False |  | Returns or sets the size of the secondary section of either a pie of pie chart or a bar of pie chart,                         as a percentage of the size of the primary pie.                        Can be a value from 5 to 200. |  
| SeriesLines | Class:Line | True |  False |  | Returns a SeriesLines object that represents the series lines for a stacked bar chart or a stacked column chart.                        Applies only to stacked bar and stacked column charts. |  
| Shadow | Boolean | True |  False |  | True if the series has a shadow. |  
| ShapeProperties | Class:LinkElement | True |  False |  | Gets the  object that holds the visual shape properties of the Series. |  
| ShowNegativeBubbles | Boolean | True |  False |  | True if negative bubbles are shown for the chart group. Valid only for bubble charts. |  
| SizeRepresents | String | True |  False |  | Gets or sets what the bubble size represents on a bubble chart. |  
| Smooth | Boolean | True |  False |  | Represents curve smoothing.                         True if curve smoothing is turned on for the line chart or scatter chart.                        Applies only to line and scatter connected by lines charts. |  
| SplitType | String | True |  False |  | Returns or sets a value that how to determine which data points are in the second pie or bar on a pie of pie or bar of                        pie chart. |  
| SplitValue | Floating | True |  False |  | Returns or sets a value that shall be used to determine which data points are in the second pie or bar on                        a pie of pie or bar of pie chart. |  
| TrendLines | Class:LinkElement | True |  False |  | Returns an object that represents a collection of all the trendlines for the series. |  
| Type | String | True |  False |  | Gets or sets a data series' type. |  
| UpBars | Class:LinkElement | True |  False |  | Returns an DropBars object that represents the up bars on a line chart.                        Applies only to line charts. |  
| Values | String | True |  False |  | Represents the data of the chart series. |  
| XErrorBar | Class:LinkElement | True |  False |  | Represents X direction error bar of the series. |  
| XValues | String | True |  False |  | Represents the x values of the chart series. |  
| YErrorBar | Class:LinkElement | True |  False |  | Represents Y direction error bar of the series. |  
| link | Class:Link | True |  False |  |  |  

**Parent Name** : [LinkElement](linkelement)

