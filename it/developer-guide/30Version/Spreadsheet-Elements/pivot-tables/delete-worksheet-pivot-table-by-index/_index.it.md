---
title: "Eliminare una tabella pivot in un foglio Excel"
second_title: "Document"
linktype: Elimina
type: docs
url: /it/pivot-tables/delete/
aliases: [/it/delete-worksheet-pivot-table-by-index/]
keywords: "Aspose.Cells, tabella pivot, eliminare, Excel, REST API"
description: "Eliminare una tabella pivot da un foglio Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include il formato della richiesta, un esempio cURL, codici di errore e frammenti di SDK per C#, Java, Python, Node.js."
weight: 70
ArticleTitle: "Come eliminare una tabella pivot in un foglio Excel con Aspose.Cells Cloud"
---

Questa REST API elimina una tabella pivot da un foglio in base al suo indice.

**Prerequisiti** – È necessario disporre di un token di accesso JWT valido per Aspose.Cells Cloud e del file Excel di destinazione memorizzato in una posizione di archiviazione supportata. Assicurarsi che il nome del file, il nome del foglio e i dettagli dell’archiviazione siano specificati correttamente prima di invocare l’API.

Le tabelle pivot rappresentano un modo potente per riepilogare i dati in un **foglio Excel**. Utilizzando Aspose.Cells Cloud, è possibile rimuovere in modo programmatico una tabella pivot non più necessaria con una singola richiesta HTTP DELETE. Questa operazione è ideale quando è necessario pulire i fogli, automatizzare la generazione di report o integrare la manipolazione di Excel nelle proprie applicazioni.

## API DeleteWorksheetPivotTable

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/it/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                           |
| --------------- | ------- | --------- | ----------------------------------------------------- |
| name            | string  | path      | Nome del documento Excel.                            |
| sheetName       | string  | path      | Nome del foglio contenente la tabella pivot.         |
| pivotTableIndex | integer | path      | Indice in base zero della tabella pivot da eliminare.|
| folder          | string  | query     | Percorso della cartella in cui è memorizzato il documento. |
| storageName     | string  | query     | Nome del servizio di archiviazione.                  |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/it#/PivotTables/DeleteWorksheetPivotTable) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Esempio di risposta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La risposta segue un semplice schema JSON:

```json
{
  "Code": integer,   // Codice di stato simile a HTTP dell'operazione
  "Status": string   // Descrizione testuale, ad esempio "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Gestione degli errori

I codici di stato di risposta comuni sono elencati di seguito:

| Stato HTTP | Descrizione                                                      |
| ---------- | ---------------------------------------------------------------- |
| 400        | Richiesta non valida – parametri mancanti o non validi.         |
| 401        | Non autorizzato – token JWT non valido o assente.               |
| 404        | Non trovato – il file, il foglio o la tabella pivot non esistono.|
| 500        | Errore interno del server – si è verificata una condizione imprevista sul server. |

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del proprio progetto. Consultare il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}
---