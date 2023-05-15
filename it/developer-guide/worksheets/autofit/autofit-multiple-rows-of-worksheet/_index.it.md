---
title: Adatta automaticamente più righe su un foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Riga
type: docs
url: /it/worksheets/autofit/rows/
aliases: [/autofit-multiple-rows-of-worksheet/]
keywords: Autofit rows on an Excel workshee
description: Aspose.Cells Cloud REST API supporta l'adattamento automatico delle righe in un foglio di lavoro Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 40
---
Questo REST API indica di adattare automaticamente le righe su un foglio di lavoro Excel.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Nome del documento.|
| foglioNome| corda| sentiero| Il nome del foglio di lavoro.|
| autoFitterOptions|| corpo| Opzioni di montaggio automatico.|
| startRow| numero intero| domanda| Inizia fila.|
| endRow| numero intero| domanda| Fine riga.|
| soloAuto| booleano| domanda| Falso|
| cartella| corda| domanda| Cartella del documento.|
| storageName| corda| domanda| nome di archiviazione.|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?firstRow=1&lastColumn=10&lastRow=7&firstColumn=1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : false}'
 
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
 
 
 
{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "094d1d9d2596d2bc485a9b1a056d901f" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "47291f603a163aa155e675f846e27ea2" >}}

{{< /tab >}}

{{< /tabs >}}




