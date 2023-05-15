---
title: Unmerge celle unite del rang
second_title: Aspose.Cells Cloud Documen
linktitle: Unmerg
type: docs
url: /it/ranges/unmerge/
aliases: [/unmerge-merged-cells-of-the-range/]
keywords: Unmerge merged cells of the range on an Excel worksheet
description: Aspose.Cells Cloud REST API supporta la separazione delle celle unite dell'intervallo in un foglio di lavoro Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
---
Questo REST API indica di separare le celle unite di questo intervallo in un foglio di lavoro Excel.
            
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/unmerge
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| nome della cartella di lavoro|
| foglioNome| corda| sentiero| nome del foglio di lavoro|
| allineare|| corpo| intervallo nel foglio di lavoro|
| cartella| corda| domanda| Cartella della cartella di lavoro.|
| storageName| corda| domanda| nome di archiviazione.|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeUnmerge) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/unmerge" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"ColumnCount\": 7, \"ColumnWidth\": 19, \"FirstColumn\": 0, \"FirstRow\": 9, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 1, \"RowHeight\": 15, \"Worksheet\": \"Sheet1\"}" 
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
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 

{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cells-cloud-gists" "cf29909cb39d0a9ad13436c14f53025d" >}}

{{< /tab >}}

{{< /tabs >}}
