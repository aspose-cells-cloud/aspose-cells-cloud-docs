---
title: "Ottieni tutte le tabelle pivot in un foglio Excel"
second_title: "Document"
linktitle: Ottieni tutte
type: docs
url: /pivot-tables/get-all/
aliases: [/get-worksheet-pivot-tables-information/]
keywords: "ottieni tutte le tabelle pivot, Aspose.Cells Cloud API, Excel PivotTable, REST API"
description: "Recupera tutte le tabelle pivot da un foglio Excel tramite l’API Aspose.Cells Cloud. Include endpoint, parametri, fasi di autenticazione, esempi cURL e SDK per l’API PivotTables."
weight: 20
ArticleTitle: "Ottieni tutte le tabelle pivot in un foglio Excel – Aspose.Cells Cloud API"
---

Una **tabella pivot** è uno strumento di sintesi dei dati in Excel che consente di riorganizzare e analizzare grandi insiemi di dati. Questa API REST recupera informazioni su **tutte** le tabelle pivot presenti in un foglio specificato.

## Sicurezza e autenticazione

Le API Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                  |
| -------------- | ------ | --------- | -------------------------------------------- |
| name           | string | path      | Nome del documento Excel.                    |
| sheetName      | string | path      | Nome del foglio di lavoro.                   |
| folder         | string | query     | Cartella in cui è memorizzato il documento.  |
| storageName    | string | query     | Nome del servizio di archiviazione.          |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) definiscono un’interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

### Richiesta

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### Risposta

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Risposte di errore

| Codice HTTP | Descrizione                                                    | Payload JSON di esempio                                     |
| ----------- | -------------------------------------------------------------- | ----------------------------------------------------------- |
| 400         | Richiesta non valida – parametro obbligatorio mancante.        | `{ "Code": "400", "Message": "Parametro obbligatorio mancante." }` |
| 401         | Non autorizzato – token non valido o mancante.                 | `{ "Code": "401", "Message": "Autenticazione non riuscita." }`      |
| 404         | Non trovato – cartella di lavoro, foglio o tabella pivot non esiste. | `{ "Code": "404", "Message": "Risorsa non trovata." }`         |
| 500         | Errore interno del server – condizione imprevista sul server.  | `{ "Code": "500", "Message": "Errore del server." }`               |

## Famiglia di SDK su cloud

L’uso di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}