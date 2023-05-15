---
title: Stile di aggiornamento per la tabella pivot
second_title: Aspose.Cells Cloud Documen
linktitle: Formatta tutto
type: docs
url: /it/pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: Update all cell style for a pivot table
description: Aspose.Cells Cloud REST API supporta l'aggiornamento di tutti gli stili di cella per una tabella pivot. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
---
Questo REST API indica lo stile `update` per la tabella pivot
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Nome del documento.|
| foglioNome| corda| sentiero| Il nome del foglio di lavoro.|
| pivotTableIndex| numero intero| sentiero| Indice della tabella pivot|
| stile|| corpo| Stile dto nel corpo della richiesta.|
| needReCalculate| booleano| domanda| Falso|
| cartella| corda| domanda| Cartella del documento.|
| storageName| corda| domanda| nome di archiviazione.|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'
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
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
