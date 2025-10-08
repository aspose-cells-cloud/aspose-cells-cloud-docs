---
title: Importa dati Json in Exce
second_title: Documen
linktitle: Importa Jso
type: docs
url: /it/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API supporta l'importazione di dati di array di stringhe in file Excel. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 40
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Importa dati Json in Excel
---
Questo foglio di lavoro REST API `import json data` in Excel.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

I parametri importanti sono descritti nella seguente tabella:

**ImportStringArrayOption**

|Nome del parametro| Percorso/Stringa di query/Corpo HTTP|Tipo|Descrizione|
|:- |:- |:- |:- |
| nome| Sentiero| corda| Il nome della cartella di lavoro|
| importJsonRequest| HTTPBody| classe| Importa richiesta json.|
| password| Stringa di query| corda| La password della cartella di lavoro.|
| cartella| Stringa di query| corda| Cartella della cartella di lavoro originale.|
| Nome di archiviazione| Stringa di query| corda| Nome dell'archivio.|
| Percorso in uscita| Stringa di query| corda| Percorso del file di output.|
|outStorageName| Stringa di query| corda| Nome di archiviazione per il file di output.|
| checkExcelRestriction| Stringa di query| corda| Controllare la restrizione Excel.|

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

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
