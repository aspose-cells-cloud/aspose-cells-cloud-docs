---
title: "Working with CellsObjectOperate Task"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API for Excel operate: cells object  operate task."
weight: 20
---

This REST API operate cells object  `task`.

**OperateObject**

|Parameter Name|Type|Description|
| :- | :- | :- |
| OperateObjectType | string | Workbook/Worksheet/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak |
| OperateObjectPosition | Object | |

**OperateObjectPosition**

|Parameter Name|Type|Description|
| :- | :- | :- |
| Workbook | Object | |
| SheetName | string | |
| ChartIndex | integer | |
| ShapeIndex | integer | |
| CellName | string | |
| ListObjectIndex | integer | |


**ChartOperateParameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| ChartIndex | integer | |
| ChartType | string | |
| UpperLeftRow | integer | |
| UpperLeftColumn | integer |  |
| LowerRightRow | integer | |
| LowerRightColumn | integer | |
| Area |string | |
| IsVertical | string | true/false |
| CategoryData |string | |
| IsAutoGetSerialName |string | true/false |
| Area |Title | |

**ListObjectOperateParameter** 

|Parameter Name|Type|Description|
| :- | :- | :- |
| ListObject | Object | |

**PageBreakOperateParameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| PageBreakType | string | |
| Index | Index | |
| Row | integer | |
| Column | integer |  |
| StartIndex | integer | |
| EndIndex | integer | |


**PageSetupOperateParameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| PageSetup | Object | |


**PivotTableOperateParameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| DestCellName | string | |
| SourceData | string | |
| TableName | string | |
| UseSameSource | string |  true/false |
| PivotTableIndex | integer | |
| PivotFieldRows | integer[] | |
| PivotFieldColumns | integer[] | |
| PivotFieldData | integer[] | |


**ShapeOperateParameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| Shape | Object | |


**WorkbookSettingsOperateParameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| WorkbookSettings | Object | |

**WorksheetOperateParameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| Name | string | |
| SheetType | string | |
| NewName | string | |
| MovingRequest | Object | |

## REST API

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/task/runtask|POST|Run Task|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. 

