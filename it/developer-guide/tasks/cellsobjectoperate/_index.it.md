---
title: Lavorare con CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API per Excel operare: celle oggetto operare attività"
weight: 20
---
Questo REST API gestisce l'oggetto celle `task`.

**OperaOggetto**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| OperateObjectType| corda| Cartella di lavoro/Foglio di lavoro/Impostapagina/Cells/Grafico/Forma/Oggetto elenco/Tabella pivot/Impostazioni cartella di lavoro/Interruzione di pagina|
| OperateObjectPosition| Oggetto||

**OperateObjectPosition**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| Cartella di lavoro| Oggetto||
| FoglioNome| corda||
| GraficoIndice| numero intero||
| Indice di forma| numero intero||
| NomeCella| corda||
| ListObjectIndex| numero intero||


**ChartOperateParameter**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| GraficoIndice| numero intero||
| Tipo di grafico| corda||
| UpperLeftRow| numero intero||
|Colonna superiore sinistra| numero intero||
| LowerRightRow| numero intero||
| Colonna in basso a destra| numero intero||
| La zona| corda||
| È verticale| corda| vero falso|
| CategoriaDati| corda||
| IsAutoGetSerialName| corda| vero falso|
| La zona| Titolo||

**ListObjectOperateParameter** 

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| ElencoOggetto| Oggetto||

**PageBreakOperateParameter**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| Tipo di interruzione di pagina| corda||
| Indice| Indice||
| Riga| numero intero||
| Colonna| numero intero||
| InizioIndice| numero intero||
| FineIndice| numero intero||


**PageSetupOperateParameter**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| Impostazione della pagina| Oggetto||


**PivotTableOperateParameter**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| DestCellName| corda||
| SourceData| corda||
| NomeTabella| corda||
| UsaSameSource| corda| vero falso|
| Indice tabella pivot| numero intero||
| PivotFieldRows|numero intero[]||
| Colonne campo pivot|numero intero[]||
|Dati del campo pivot|numero intero[]||


**Parametro ShapeOperate**


|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| Forma| Oggetto||


**WorkbookSettingsOperateParameter**


|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| Impostazioni della cartella di lavoro| Oggetto||

**Foglio di lavoroOperateParameter**


|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| Nome| corda||
| Tipo di foglio| corda||
| Nuovo nome| corda||
| MovingRequest| Oggetto||

## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Collegamento alla risorsa**|
|:- |:- |:- |:- |
|/celle/attività/runtask|INVIARE|Esegui attività|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

