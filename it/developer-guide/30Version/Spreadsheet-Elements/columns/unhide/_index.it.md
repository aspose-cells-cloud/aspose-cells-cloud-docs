---
title: "Rivela colonne in un foglio di lavoro Excel"
ArticleTitle: "Rivela colonne in un foglio di lavoro Excel - Aspose.Cells Cloud API"
second_title: "Documenti"
linktitle: "Rivela"
type: docs
url: /it/columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, API cloud, rivela colonne, Excel, REST, SDK"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per rivelare le colonne in un foglio di lavoro Excel. Include i dettagli della richiesta, un esempio cURL e frammenti di codice SDK per diversi linguaggi di programmazione."
weight: 50
---

Questa API REST rivela le colonne del foglio di lavoro.

**Prerequisiti** – Tutti gli endpoint di Aspose.Cells Cloud richiedono HTTPS e un token di accesso OAuth 2.0 valido. Assicurati di aver ottenuto un token di accesso e di averlo incluso nell'header `Authorization` delle tue richieste.

## API PostUnhideWorksheetColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                           |
| -------------- | ------- | --------- | ----------------------------------------------------- |
| name           | string  | path      | Nome del workbook.                                    |
| sheetName      | string  | path      | Nome del foglio di lavoro.                            |
| startColumn    | integer | query     | Indice della prima colonna da elaborare.              |
| totalColumns   | integer | query     | Numero di colonne da elaborare.                       |
| width          | number  | query     | Larghezza desiderata della colonna (valore predefinito = 50,0). |
| folder         | string  | query     | Cartella contenente il documento.                     |
| storageName    | string  | query     | Nome del servizio di archiviazione.                   |

La <a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di stato HTTP tipici**

| Codice | Descrizione                                            |
|--------|--------------------------------------------------------|
| 200    | OK – Le colonne sono state rivelate correttamente.    |
| 400    | Richiesta non valida – Parametri non validi.           |
| 401    | Non autorizzato – Token mancante o non valido.         |
| 404    | Non trovato – Workbook o foglio di lavoro non trovato. |
| 500    | Errore interno del server – Guasto imprevisto.        |

## Famiglia di SDK per il Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}