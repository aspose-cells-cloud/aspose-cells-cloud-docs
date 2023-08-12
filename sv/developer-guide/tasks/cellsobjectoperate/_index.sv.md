---
title: Arbeta med CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API för Excel operera: celler objekt operera uppgift"
weight: 20
---
Detta REST API opererar cellobjekt `task`.

**OperateObject**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| OperateObjectType| sträng| Arbetsbok/Arbetsblad/Sidinställningar/Cells/Diagram/Shape/ListObject/PivotTable/Arbetsboksinställningar/Page Break|
| OperateObjectPosition| Objekt||

**OperateObjectPosition**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Arbetsbok| Objekt||
| SheetName| sträng||
| ChartIndex| heltal||
| ShapeIndex| heltal||
| Cellnamn| sträng||
| ListObjectIndex| heltal||


**ChartOperateParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| ChartIndex| heltal||
| ChartType| sträng||
| UpperLeftRow| heltal||
|Övre vänstra kolumnen| heltal||
| Nedre högerrad| heltal||
| Nedre högerkolumn| heltal||
| Område| sträng||
| Är Vertikal| sträng| sant falskt|
| CategoryData| sträng||
| IsAutoGetSerialName| sträng| sant falskt|
| Område| Titel||

**ListObjectOperateParameter** 

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| ListObject| Objekt||

**PageBreakOperateParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| PageBreakType| sträng||
| Index| Index||
| Rad| heltal||
| Kolumn| heltal||
| Startindex| heltal||
| EndIndex| heltal||


**PageSetupOperateParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Utskriftsformat| Objekt||


**PivotTableOperateParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| DestCellName| sträng||
| Källdata| sträng||
| Tabellnamn| sträng||
| UseSameSource| sträng| sant falskt|
| PivotTableIndex| heltal||
| PivotFieldRows|heltal[]||
| Pivotfältkolumner|heltal[]||
|PivotFieldData|heltal[]||


**ShapeOperateParameter**


|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Form| Objekt||


**WorkbookSettingsOperateParameter**


|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Arbetsbok Inställningar| Objekt||

**ArbetsbladOperateParameter**


|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| namn| sträng||
| SheetType| sträng||
| Nytt namn| sträng||
| Flyttförfrågan| Objekt||

## REST API

|**API**|**Typ**|**Beskrivning**|**Resurslänk**|
|:- |:- |:- |:- |
|/cells/task/runtask|POSTA|Kör uppgift|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

