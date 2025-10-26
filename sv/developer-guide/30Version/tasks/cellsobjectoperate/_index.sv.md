---
title: Arbeta med CellsObjectOperate Tas
second_title: Documen
type: docs
url: /sv/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API för Excel operate: cells object operate task"
weight: 20
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Arbeta med CellsObjectOperate-uppgift
---
Detta REST API opererar celler-objekt `task`.

**OperateObject**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| OperateObjectType| sträng|Arbetsbok/Arbetsblad/Sidinställningar/Cells/Diagram/Form/Listobjekt/Pivottabell/Arbetsboksinställningar/Sidbrytning|
| OperateObjectPosition| Objekt||

**OperateObjectPosition**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Arbetsbok| Objekt||
| Arknamn| sträng||
| Diagramindex| heltal||
| Formindex| heltal||
| Cellnamn| sträng||
| ListObjectIndex| heltal||


**DiagramOpereraParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Diagramindex| heltal||
| Diagramtyp| sträng||
| Övre vänsterrad| heltal||
| Övre vänsterkolumn| heltal||
| Nedre högerrad| heltal||
| Nedre högerkolumn| heltal||
| Område| sträng||
| ÄrVertikal| sträng| sant/falskt|
| KategoriData| sträng||
| ÄrAutoGetSeriellnamn| sträng| sant/falskt|
| Område| Titel||

**ListObjectOperateParameter** 

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| ListObject| Objekt||

**SidbrytningOpereraParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Sidbrytningstyp| sträng||
| Index| Index||
| Rad| heltal||
| Kolumn| heltal||
| Startindex| heltal||
| Slutindex| heltal||


**SidinställningarOpereraParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Sidinställningar| Objekt||


**PivottabellOpereraParameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| DestCellName| sträng||
| Källdata| sträng||
| Tabellnamn| sträng||
| AnvändSammaKälla| sträng| sant/falskt|
| PivottabellIndex| heltal||
| PivotfältRader|heltal[]||
| Pivotfältkolumner|heltal[]||
| Pivotfältdata|heltal[]||


**FormOpereraParameter**


|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Form| Objekt||


**ArbetsboksinställningarOpereraParameter**


|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Arbetsboksinställningar| Objekt||

**ArbetsbladOpereraParameter**


|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Namn| sträng||
| Arktyp| sträng||
| Nytt namn| sträng||
| Flyttförfrågan| Objekt||

## REST API

|**API**|**Typ**|**Beskrivning**|**Resurslänk**|
|:- |:- |:- |:- |
|/celler/uppgift/köruppgift|POSTA|Kör uppgift|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

