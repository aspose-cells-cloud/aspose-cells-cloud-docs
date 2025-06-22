---
title: Importa dati utilizzando storage
second_title: Aspose.Cells Cloud Documen
linktitle: Importa dati con archiviazione
type: docs
url: /it/import-data-with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/,/import/with-using-storage/]
description: "Cells.Cloud API per Excel opera: Importa dati nel foglio di lavoro Excel"
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Importa dati con utilizzo di storage
---
Questo REST API indica `import data` nel file Excel.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| cartella| corda| domanda||
| Nome di archiviazione| corda| domanda| nome di archiviazione.|
| importa dati|| corpo||

**Parametri delle opzioni di importazione dei dati** sono descritti in[il collegamento di riferimento](/cells/it/import/#import-data-option-parameter).

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
