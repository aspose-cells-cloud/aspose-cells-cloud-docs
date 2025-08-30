---
title: Lavorare con CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API per Excel opera: celle oggetto opera compito"
weight: 20
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Lavorare con l'attività CellsObjectOperate
---
Questo REST API gestisce le celle oggetto `task`.

**OperateObject**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| OperateObjectType| corda| Cartella di lavoro/Foglio di lavoro/Imposta pagina/Cells/Grafico/Forma/Oggetto elenco/Tabella pivot/Impostazioni cartella di lavoro/Interruzione di pagina|
| OperateObjectPosition| Oggetto||

**OperateObjectPosition**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Quaderno di lavoro| Oggetto||
| NomeFoglio| corda||
| Indice del grafico| intero||
| Indice di forma| intero||
| NomeCella| corda||
| IndiceOggettoElenco| intero||


**ChartOperateParameter**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Indice del grafico| intero||
| Tipo di grafico| corda||
| Riga superiore sinistra| intero||
| Colonna in alto a sinistra| intero||
| Riga inferiore destra| intero||
| Colonna inferiore destra| intero||
| Zona| corda||
| IsVertical| corda| vero/falso|
| CategoriaDati| corda||
| IsAutoGetSerialName| corda| vero/falso|
| Zona| Titolo||

**ListObjectOperateParameter** 

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| ElencoOggetto| Oggetto||

**Parametro di operazione di interruzione di pagina**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Tipo di interruzione di pagina| corda||
| Indice| Indice||
| Riga| intero||
| Colonna| intero||
| Indice di inizio| intero||
| EndIndex| intero||


**Parametro di operazione di impostazione della pagina**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Impostazione pagina| Oggetto||


**PivotTableOperateParameter**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| NomeCellaDest| corda||
| Dati di origine| corda||
| NomeTabella| corda||
| UsaSameSource| corda| vero/falso|
| IndiceTabellaPivot| intero||
| PivotFieldRows|intero[]||
| Colonne di campi pivot|intero[]||
| Dati del campo pivot|intero[]||


**Parametro di funzionamento forma**


|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Forma| Oggetto||


**Impostazioni cartella di lavoro Opera Parametro**


|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Impostazioni cartella di lavoro| Oggetto||

**Foglio di lavoroOperateParameter**


|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Nome| corda||
| Tipo di foglio| corda||
| Nuovo nome| corda||
| Richiesta di trasloco| Oggetto||

## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Link alla risorsa**|
|:- |:- |:- |:- |
|/cells/task/runtask|INVIARE|Esegui attività|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

