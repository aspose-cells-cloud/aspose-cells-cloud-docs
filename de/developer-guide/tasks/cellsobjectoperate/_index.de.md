---
title: Arbeiten mit CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API für Excel Operate: Zellenobjekt-Operate-Task"
weight: 20
---
Dieses REST API betreibt das Zellenobjekt `task`.

**OperateObject**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| OperateObjectType| Zeichenfolge| Workbook/Worksheet/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak|
| OperateObjectPosition| Objekt||

**OperateObjectPosition**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Arbeitsmappe| Objekt||
| Blattname| Zeichenfolge||
| ChartIndex| ganze Zahl||
| ShapeIndex| ganze Zahl||
| Zellenname| Zeichenfolge||
| ListObjectIndex| ganze Zahl||


**ChartOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| ChartIndex| ganze Zahl||
| Diagramm Typ| Zeichenfolge||
| UpperLeftRow| ganze Zahl||
| UpperLeftColumn| ganze Zahl||
| LowerRightRow| ganze Zahl||
| LowerRightColumn| ganze Zahl||
| Bereich| Zeichenfolge||
| IsVertical| Zeichenfolge| wahr falsch|
| Kategoriedaten| Zeichenfolge||
| IsAutoGetSerialName| Zeichenfolge| wahr falsch|
| Bereich| Titel||

**ListObjectOperateParameter** 

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| ListObject| Objekt||

**PageBreakOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| PageBreakType| Zeichenfolge||
| Index| Index||
| Reihe| ganze Zahl||
| Spalte| ganze Zahl||
| Startindex| ganze Zahl||
| EndIndex| ganze Zahl||


**PageSetupOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Seiteneinrichtung| Objekt||


**PivotTableOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Zielzellenname| Zeichenfolge||
| Quelldaten| Zeichenfolge||
| Tabellenname| Zeichenfolge||
| UseSameSource| Zeichenfolge| wahr falsch|
| PivotTableIndex| ganze Zahl||
| PivotFieldRows|ganze Zahl[]||
| PivotFieldColumns|ganze Zahl[]||
|PivotFieldData|ganze Zahl[]||


**ShapeOperateParameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Form| Objekt||


**WorkbookSettingsOperateParameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Arbeitsmappeneinstellungen| Objekt||

**WorksheetOperateParameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Name| Zeichenfolge||
| SheetType| Zeichenfolge||
| Neuer Name| Zeichenfolge||
| Umzugsanfrage| Objekt||

## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/cells/task/runtask|POST|Aufgabe ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht die Durchführung von REST-Interaktionen direkt über einen Webbrowser.

