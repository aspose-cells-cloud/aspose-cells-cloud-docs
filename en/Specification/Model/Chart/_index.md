---
title: "Chart"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/chart/
description: ""
weight: 50
---

## **chart**

 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| AutoScaling | Boolean | True |  False |  | True if Microsoft Excel scales a 3-D chart so that it's closer in size to the equivalent 2-D chart.                         The RightAngleAxes property must be True. |  
| BackWall | Class:LinkElement | True |  False |  | Returns a  object that represents the back wall of a 3-D chart. |  
| CategoryAxis | Class:LinkElement | True |  False |  | Gets the chart's X axis. |  
| ChartArea | Class:LinkElement | True |  False |  | Gets the chart area in the worksheet. |  
| ChartDataTable | Class:LinkElement | True |  False |  | Represents the chart data table. |  
| ChartObject | Class:LinkElement | True |  False |  | Represents the chartShape; |  
| DepthPercent | Integer | True |  False |  | Represents the depth of a 3-D chart as a percentage of the chart width (between 20 and 2000 percent). |  
| Elevation | Integer | True |  False |  | Represents the elevation of the 3-D chart view, in degrees. |  
| FirstSliceAngle | Integer | True |  False |  | Gets or sets the angle of the first pie-chart or doughnut-chart slice, in degrees (clockwise from vertical).                         Applies only to pie, 3-D pie, and doughnut charts, 0 to 360. |  
| Floor | Class:LinkElement | True |  False |  | Returns a  object that represents the walls of a 3-D chart. |  
| GapDepth | Integer | True |  False |  | Gets or sets the distance between the data series in a 3-D chart, as a percentage of the marker width.                        The value of this property must be between 0 and 500. |  
| GapWidth | Integer | True |  False |  | Returns or sets the space between bar or column clusters, as a percentage of the bar or column width.                        The value of this property must be between 0 and 500. |  
| HeightPercent | Integer | True |  False |  | Returns or sets the height of a 3-D chart as a percentage of the chart width (between 5 and 500 percent). |  
| HidePivotFieldButtons | Boolean | True |  False |  | Indicates whether hide the pivot chart field buttons only when the chart is PivotChart. |  
| Is3D | Boolean | True |  False |  | Indicates whether the chart is a 3d chart. |  
| IsRectangularCornered | Boolean | True |  False |  | Gets or sets a value indicating whether the chart area is rectangular cornered.                        Default is true. |  
| Legend | Class:LinkElement | True |  False |  | Gets the chart legend. |  
| Name | String | True |  False |  |  |  
| NSeries | Class:LinkElement | True |  False |  | Gets a  collection representing the data series in the chart. |  
| PageSetup | Class:LinkElement | True |  False |  | Represents the page setup description in this chart. |  
| Perspective | Integer | True |  False |  | Returns or sets the perspective for the 3-D chart view. Must be between 0 and 100.                        This property is ignored if the RightAngleAxes property is True. |  
| PivotSource | String | True |  False |  | The source is the data of the pivotTable.                        If PivotSource is not empty ,the chart is PivotChart. |  
| Placement | String | True |  False |  | Represents the way the chart is attached to the cells below it. |  
| PlotArea | Class:LinkElement | True |  False |  | Gets the chart's plot area which includes axis tick labels. |  
| PlotEmptyCellsType | String | True |  False |  | Gets and sets  how to plot the empty cells. |  
| PlotVisibleCells | Boolean | True |  False |  | Indicates whether only plot visible cells. |  
| PrintSize | String | True |  False |  | Gets and sets the printed chart size. |  
| RightAngleAxes | Boolean | True |  False |  | True if the chart axes are at right angles. Applies only for 3-D charts(except Column3D and 3-D Pie Charts). |  
| RotationAngle | Integer | True |  False |  | Represents the rotation of the 3-D chart view (the rotation of the plot area around the z-axis, in degrees). |  
| SecondCategoryAxis | Class:LinkElement | True |  False |  | Gets the chart's second X axis. |  
| SecondValueAxis | Class:LinkElement | True |  False |  | Gets the chart's second Y axis. |  
| SeriesAxis | Class:LinkElement | True |  False |  | Gets the chart's series axis. |  
| Shapes | Class:LinkElement | True |  False |  | Returns all drawing shapes in this chart. |  
| ShowDataTable | Boolean | True |  False |  | Gets or sets a value indicating whether the chart displays a data table. |  
| ShowLegend | Boolean | True |  False |  | Gets or sets a value indicating whether the chart legend will be displayed. Default is true. |  
| SideWall | Class:LinkElement | True |  False |  | Returns a  object that represents the side wall of a 3-D chart. |  
| SizeWithWindow | Boolean | True |  False |  | True if Microsoft Excel resizes the chart to match the size of the chart sheet window. |  
| Style | Integer | True |  False |  | Gets and sets the builtin style. |  
| Title | Class:LinkElement | True |  False |  |  |  
| Type | String | True |  False |  |  |  
| ValueAxis | Class:LinkElement | True |  False |  | Gets the chart's Y axis. |  
| Walls | Class:LinkElement | True |  False |  | Returns a  object that represents the walls of a 3-D chart. |  
| WallsAndGridlines2D | Boolean | True |  False |  | True if gridlines are drawn two-dimensionally on a 3-D chart. |  
| link | Class:Link | True |  False |  |  |  

**Parent Name** : (LinkElement)[linkelement]

