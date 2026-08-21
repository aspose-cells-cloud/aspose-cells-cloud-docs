---
title: "Ottenere il numero di pagine di un foglio di calcolo Excel"
second_title: "Document"
linktype: "PageCount"
type: docs
url: /it/worksheets/page-count/
keywords: "Aspose.Cells, API Excel, numero di pagine del foglio di calcolo, REST, SDK cloud, impaginazione Excel"
description: "Recuperare il numero di pagine stampabili in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include il formato della richiesta HTTPS, i passaggi per l'autenticazione, un esempio cURL, la risposta JSON completa, i codici di stato e esempi di codice SDK."
weight: 10
ArticleTitle: "Ottenere il numero di pagine di un foglio di calcolo Excel – Aspose.Cells Cloud API"
---

Questa API REST restituisce il **numero di pagine** per un foglio di calcolo.

**Autenticazione:** Tutti gli endpoint di Aspose.Cells Cloud richiedono un token Bearer ottenuto tramite il flusso OAuth2. Includere il token nell'intestazione `Authorization`, come mostrato nell'esempio cURL riportato di seguito.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### Parametri della richiesta

| Parametro   | Tipo   | Posizione | Descrizione                              |
| ----------- | ------ | --------- | ---------------------------------------- |
| name        | string | path      | Nome del documento.                      |
| sheetName   | string | path      | Nome del foglio di calcolo.              |
| folder      | string | query     | Cartella contenente il documento.        |
| storageName | string | query     | Nome dello storage.                      |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio riportato di seguito mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Dettagli della risposta

| Codice HTTP | Significato                                         |
| ----------- | --------------------------------------------------- |
| **200**     | Successo – restituisce il payload JSON mostrato sopra. |
| **401**     | Non autorizzato – token mancante o non valido.      |
| **404**     | Non trovato – il file o il foglio di calcolo non esiste. |
| **500**     | Errore interno del server – condizione imprevista del server. |

### Cronologia delle versioni

_API versione **v3.0** (rilasciata nel 2025). Se si utilizza una versione più recente, fare riferimento alla documentazione aggiornata dell'endpoint._

## Famiglia di SDK cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli a basso livello in modo da potersi concentrare sulla logica aziendale. Consultare la [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Note

- Il numero di pagine riflette il layout stampabile, tenendo conto delle interruzioni di pagina, dei margini e della scala. Le righe o le colonne nascoste possono influenzare il risultato.
- Prima di effettuare la richiesta, assicurarsi che il foglio di calcolo di destinazione esista e che il file sia archiviato nella cartella e nello `storageName` specificati.