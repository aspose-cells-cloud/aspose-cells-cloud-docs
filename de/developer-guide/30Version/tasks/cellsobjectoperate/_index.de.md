---
title: Arbeiten mit CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API für Excel betreiben: Zellen Objekt betreiben Aufgabe"
weight: 20
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Arbeiten mit CellsObjectOperate Task
---
Dieses REST API betreibt Zellenobjekt `task`.

**OperateObject**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| OperateObjectType| Schnur| Arbeitsmappe/Arbeitsblatt/Seiteneinrichtung/Cells/Diagramm/Form/Listenobjekt/PivotTable/Arbeitsmappeneinstellungen/Seitenumbruch|
| OperateObjectPosition| Objekt||

**OperateObjectPosition**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Arbeitsmappe| Objekt||
| Blattname| Schnur||
| ChartIndex| ganze Zahl||
| Formindex| ganze Zahl||
| Zellenname| Schnur||
| ListObjectIndex| ganze Zahl||


**ChartOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| ChartIndex| ganze Zahl||
| Diagrammtyp| Schnur||
| Obere Linke Zeile| ganze Zahl||
| Obere linke Spalte| ganze Zahl||
| UntereRechteReihe| ganze Zahl||
| Untere Rechte Spalte| ganze Zahl||
| Bereich| Schnur||
| IsVertical| Schnur| wahr/falsch|
| KategorieDaten| Schnur||
| IsAutoGetSerialName| Schnur| wahr/falsch|
| Bereich| Titel||

**ListObjectOperateParameter** 

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| ListObject| Objekt||

**PageBreakOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Seitenumbruchtyp| Schnur||
| Index| Index||
| Reihe| ganze Zahl||
| Spalte| ganze Zahl||
| StartIndex| ganze Zahl||
| EndIndex| ganze Zahl||


**SeiteSetupOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Seiteneinrichtung| Objekt||


**PivotTableOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Zielzellenname| Schnur||
| Quelldaten| Schnur||
| Tabellenname| Schnur||
| UseSameSource| Schnur| wahr/falsch|
| PivotTableIndex| ganze Zahl||
| PivotFieldRows|ganze Zahl[]||
| PivotFieldColumns|ganze Zahl[]||
| PivotFieldData|ganze Zahl[]||


**ShapeOperateParameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Form| Objekt||


**ArbeitsmappeneinstellungenBetriebsparameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Arbeitsmappeneinstellungen| Objekt||

**ArbeitsblattOperateParameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Name| Schnur||
| Blatttyp| Schnur||
| NeuerName| Schnur||
| Umzugsanfrage| Objekt||

## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/Zellen/Aufgabe/Ausführen der Aufgabe|POST|Task ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

