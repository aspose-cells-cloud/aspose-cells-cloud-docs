---
title: Convertire la tabella in tabella pivot
second_title: Aspose.Cells Cloud Documen
linktitle: Convertire
type: docs
url: /it/pivot-tables/convert-table-to-pivottable/
aliases: [/create-a-pivottable-with-table/,/create-new-pivot-table-with-list-object-as-source-data/]
keywords: Create a pivot table with list object. Convert list object to pivot table
description: Aspose.Cells Cloud REST API supporta la creazione di una tabella pivot con oggetto elenco. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 60
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Converti tabella in tabella pivot
---
Questo REST API indica di creare un `pivottable` con oggetto elenco.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| Nome del foglio| corda| sentiero||
| indiceOggettoElenco| intero| sentiero||
| Nome foglio di destinazione| corda| domanda||
| richiesta|| corpo||
| cartella| corda| domanda||
| Nome di archiviazione| corda| domanda| nome di archiviazione.|
 
 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api-qa.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \ \
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
 
## Famiglia Cloud SDK
 
 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 
