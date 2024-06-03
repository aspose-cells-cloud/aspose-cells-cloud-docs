---
title: Arbeiten mit CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API für Excel bedienen: Zellen Objekt bedienen Aufgabe"
weight: 20
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Arbeiten mit CellsObjectOperate Task
---
Dieses REST API betreibt Zellenobjekt `task`.

**Objekt bedienen**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Objekttyp bedienen| Schnur| Arbeitsmappe/Arbeitsblatt/Seiteneinrichtung/Cells/Diagramm/Form/Listenobjekt/PivotTable/Arbeitsmappeneinstellungen/Seitenumbruch|
| Objektposition bedienen| Objekt||

**Objektposition bedienen**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Arbeitsmappe| Objekt||
| Blattname| Schnur||
| ChartIndex| ganze Zahl||
| FormIndex| ganze Zahl||
| Zellenname| Schnur||
| Listenobjektindex| ganze Zahl||


**ChartOperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| ChartIndex| ganze Zahl||
|Diagramm Typ| Schnur||
| Obere Linke Zeile| ganze Zahl||
| Obere Linke Spalte| ganze Zahl||
| UntereRechteReihe| ganze Zahl||
| Untere Rechte Spalte| ganze Zahl||
| Bereich| Schnur||
| IstVertikal| Schnur| wahr falsch|
| KategorieDaten| Schnur||
| IsAutoGetSerialName| Schnur| wahr falsch|
| Bereich| Titel||

**ListObjectOperateParameter** 

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Listenobjekt| Objekt||

**Seitenumbruch-OperateParameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Seitenumbruchtyp| Schnur||
| Index| Index||
| Reihe| ganze Zahl||
| Spalte| ganze Zahl||
| Startindex| ganze Zahl||
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
| UseSameSource| Schnur| wahr falsch|
| PivotTableIndex| ganze Zahl||
| PivotFieldRows|ganze Zahl[]||
| PivotFieldColumns|ganze Zahl[]||
| PivotFieldData|ganze Zahl[]||


**ShapeOperateParameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Form| Objekt||


**ArbeitsmappeneinstellungenBedienparameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Arbeitsmappeneinstellungen| Objekt||

**ArbeitsblattOperateParameter**


|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Name| Schnur||
| Blatttyp| Schnur||
| Neuer Name| Schnur||
| Umzugsanfrage| Objekt||

## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/Zellen/Aufgabe/Runtask|POST|Aufgabe ausführen|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

