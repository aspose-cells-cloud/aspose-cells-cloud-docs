---
title: Lavorare con CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API per Excel operare: attività di operazione oggetto celle"
weight: 20
---
Questo REST API gestisce le celle oggetto `task`.

**OperaOggetto**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| OperareObjectType| corda| Cartella di lavoro/Foglio di lavoro/PageSetup/Cells/Grafico/Forma/OggettoElenco/TabellaPivot/WorkbookSettings/PageBreak|
| OperarePosizioneOggetto| Oggetto||

**OperarePosizioneOggetto**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Cartella di lavoro| Oggetto||
| NomeFoglio| corda||
| ChartIndex| numero intero||
| ShapeIndex| numero intero||
| NomeCella| corda||
| ElencoOggettoIndice| numero intero||


**ChartOperateParametro**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| ChartIndex| numero intero||
| ChartType| corda||
| Riga superiore sinistra| numero intero||
| Colonna superiore sinistra| numero intero||
| Riga InferioreDestra| numero intero||
| Colonna inferiore destra| numero intero||
| La zona| corda||
| È verticale| corda| vero falso|
| CategoriaDati| corda||
| IsAutoGetSerialName| corda| vero falso|
| La zona| Titolo||

**ParametroListObjectOperate** 

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| ElencoOggetto| Oggetto||

**Parametro PageBreakOperate**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| PageBreakType| corda||
| Indice| Indice||
| Riga| numero intero||
| Colonna| numero intero||
| InizioIndice| numero intero||
| EndIndex| numero intero||


**PageSetupOperateParametro**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Impostazione della pagina| Oggetto||


**ParametroOperateTabellaPivot**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| NomeCellaDest| corda||
| Dati di origine| corda||
| NomeTabella| corda||
| UsaSameSource| corda| vero falso|
| Indice tabella pivot| numero intero||
| Righe del campo pivot|numero intero[]||
| Colonne del campo pivot|numero intero[]||
|Dati campo pivot|numero intero[]||


**ShapeOperateParametro**


|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Forma| Oggetto||


**WorkbookSettingsOperateParameter**


|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Impostazioni cartella di lavoro| Oggetto||

**Foglio di lavoroOperateParametro**


|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Nome| corda||
| Tipo Foglio| corda||
| Nuovo nome| corda||
| MovingRequest| Oggetto||

## RESTO API

|**API**|**Tipo**|**Descrizione**|**Collegamento alle risorse**|
|:- |:- |:- |:- |
|/cells/attività/runtask|INVIARE|Esegui attività|[Attività PostEsegui](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

