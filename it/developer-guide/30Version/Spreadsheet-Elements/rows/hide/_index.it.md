---
title: "Nascondere righe in un foglio di Excel"
second_title: "Documento"
linktitle: "Nascondi"
type: docs
url: /it/rows/hide/
aliases: [  /it/hide-rows-in-excel-worksheet/ ]
keywords: "nascondere righe, Aspose.Cells Cloud, API Excel, REST, SDK"
description: "Scopri come nascondere una o più righe in un foglio di Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempio cURL, frammenti di codice SDK, parametri, autenticazione, dettagli della risposta e gestione degli errori."
weight: 40
ArticleTitle: "Nascondere righe in un foglio di Excel utilizzando l'API Aspose.Cells Cloud"
---

Questa API REST nasconde le righe in un foglio di Excel.

**Prerequisiti:** Un token JWT Bearer valido ottenuto dall'endpoint OAuth di Aspose Cloud, il foglio di calcolo memorizzato nell'archivio Aspose Cloud e il nome del foglio di lavoro contenente le righe da nascondere. L'API funziona con file Excel nei formati XLS, XLSX e altri formati supportati.

## API PostHideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Parametro       | Tipo    | Posizione | Descrizione                                                         |
| --------------- | ------- | -------- | ------------------------------------------------------------------- |
| **name**        | string  | path     | Nome del file del foglio di calcolo.                                |
| **sheetName**   | string  | path     | Nome del foglio di lavoro contenente le righe da nascondere.        |
| **startrow**    | integer | query    | Indice in base zero della prima riga da nascondere.                 |
| **totalRows**   | integer | query    | Numero di righe consecutive da nascondere, a partire da **startrow**. |
| **folder**      | string  | query    | Cartella nell'archivio in cui si trova il foglio di calcolo.        |
| **storageName** | string  | query    | Nome del servizio di archiviazione.                                 |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) fornisce un'interfaccia di programmazione pubblicamente accessibile che consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per chiamare i servizi web di Aspose.Cells. L'API richiede un token JWT Bearer ottenuto dall'endpoint OAuth di Aspose Cloud; tale token deve essere incluso nell'intestazione `Authorization`. L'esempio seguente mostra come nascondere una riga utilizzando cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di stato della risposta**

| Codice | Descrizione |
|--------|-------------|
| 200 | Successo – righe nascoste |
| 400 | Richiesta non valida – parametri non validi |
| 401 | Non autorizzato – token JWT mancante o non valido |
| 404 | Non trovato – il foglio di calcolo o il foglio di lavoro non esiste |
| 500 | Errore del server – fallimento durante l'elaborazione interna |

Una chiamata riuscita restituisce un oggetto JSON contenente i campi `Code` e `Status`. In caso di errore, la risposta include campi aggiuntivi come `Message` e i codici di stato HTTP appropriati (ad esempio 400, 401, 404, 500).

**Note:** Assicurarsi che il valore di `startrow` rientri nell'intervallo di righe del foglio di lavoro; in caso contrario l'API restituirà un errore 400. Gli indici di riga sono in base zero, pertanto `startrow=0` si riferisce alla prima riga.

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per integrare questa funzionalità nella propria applicazione. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come nascondere le righe utilizzando vari SDK. (I nomi dei file di esempio fanno riferimento a “Unhide” a causa di una convenzione di denominazione legacy; il codice contenuto in ogni gist esegue l'operazione **Hide**.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}