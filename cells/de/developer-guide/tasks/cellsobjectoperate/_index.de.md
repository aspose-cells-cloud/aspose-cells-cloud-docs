---
title: Arbeiten mit CellsObjectOperate-Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API für Excel Operate: Cells Object Operate Task"
weight: 20
---
Dieses REST API betreibt Zellenobjekt `task`.

**OperateObject**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| OperateObjectType| Schnur| Workbook/Worksheet/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak|
| OperateObjectPosition| Objekt||

**OperateObjectPosition**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Arbeitsmappe| Objekt||
| Blattname| Schnur||
| ChartIndex| ganze Zahl||
| ShapeIndex| ganze Zahl||
| Zellenname| Schnur||
| ListObjectIndex| ganze Zahl||


**ChartOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| ChartIndex| ganze Zahl||
| Diagramm Typ| Schnur||
| ObereLinkeReihe| ganze Zahl||
|UpperLeftColumn| ganze Zahl||
| LowerRightRow| ganze Zahl||
| LowerRightColumn| ganze Zahl||
| Bereich| Schnur||
| IstVertikal| Schnur| wahr falsch|
| Kategoriedaten| Schnur||
| IsAutoGetSerialName| Schnur| wahr falsch|
| Bereich| Titel||

**ListObjectOperateParameter** 

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Listenobjekt| Objekt||

**PageBreakOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Seitenumbruchtyp| Schnur||
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
| Zielzellenname| Schnur||
| Quelldaten| Schnur||
| Tabellenname| Schnur||
| Verwenden Sie die gleiche Quelle| Schnur| wahr falsch|
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
| Name| Schnur||
| Blatttyp| Schnur||
| Neuer Name| Schnur||
| Umzugsanfrage| Objekt||

## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcen-Link**|
|:- |:- |:- |:- |
|/cells/task/runtask|POST|Aufgabe ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.

