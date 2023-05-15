---
title: Aggiorna
type: docs
url: /it/comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: REST API, spreadsheets, excel, update commen
description: "Cells.Cloud API per Excel opera: aggiornamento commento"
weight: 30
---
Questo REST API indica il commento della cella del foglio di lavoro di aggiornamento.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Il nome del documento.|
| foglioNome| corda| sentiero| Il nome del foglio di lavoro.|
| cellName| corda| sentiero| Il nome della cella|
| commento|| corpo| Oggetto commento|
| cartella| corda| domanda| La cartella dei documenti.|
| storageName| corda| domanda| nome di archiviazione.|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"\
-d "{ \"CellName\": \"a1\", \"Author\": \"test\", \"HtmlNote\": \"string\", \"Note\": \"this is a comment\", \"AutoSize\": true, \"IsVisible\": true, \"Width\": 10, \"Height\": 10}"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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

{{< gist "aspose-cells-cloud-gists" "bf512f63ac7d0c31f9a0f1008cd3e031" >}}

{{< /tab >}}

{{< /tabs >}}




