---
title: Importa i dati Json in Exce
second_title: Aspose.Cells Cloud Documen
linktitle: Importa Jso
type: docs
url: /it/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API supporta l'importazione di dati di array di stringhe nei file Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 40
---
Questo REST API `import json data` nel foglio di lavoro Excel.


## RSETAPI

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

I parametri importanti sono descritti nella tabella seguente:


**ImportStringArrayOption**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| nome| corda| Il nome della cartella di lavoro|
| importJsonRequest| classe| Richiesta di importazione JSON.|
| parola d'ordine| corda| La password della cartella di lavoro.|
| cartella| corda|Cartella della cartella di lavoro originale.|
| storageName| corda| Nome dell'archivio.|
| outPath| corda| Percorso del file di output.|
| outStorageName| corda| Nome di archiviazione per il file di output.|
| checkExcelRestrizione| corda| Controlla la restrizione Excel.|


**Esempio**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## Famiglia di SDK Cloud

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.

I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:





