---
title: "Adattamento automatico di più righe in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Righe"
type: docs
url: /it/worksheets/autofit/rows/
aliases: [  /it/autofit-multiple-rows-of-worksheet/ ]
keywords: "adattamento automatico righe, Excel, Aspose.Cells Cloud, API REST, foglio di lavoro, foglio elettronico"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per eseguire l'adattamento automatico di più righe in un foglio di lavoro Excel. Include la sintassi della richiesta, i parametri, un esempio cURL, frammenti di codice per gli SDK e la gestione degli errori."
weight: 40
ArticleTitle: "Adattamento automatico di più righe in un foglio di lavoro Excel – Documentazione API Aspose.Cells Cloud"
---

Questa API REST regola automaticamente l'altezza delle righe in un foglio di lavoro Excel.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **Parametri della richiesta**

| Nome parametro        | Tipo    | Posizione | Descrizione                                                                                                                          | Obbligatorio |
| --------------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------ |
| **name**              | string  | path     | Nome del file Excel.                                                                                                                 | ✔ |
| **sheetName**         | string  | path     | Nome del foglio di lavoro.                                                                                                           | ✔ |
| **autoFitterOptions** | object  | body     | Opzioni che controllano il modo in cui vengono eseguite l'adattamento automatico delle righe (ad esempio, ignorare le righe nascoste). Vedi la breve descrizione dei campi di seguito. | ✖ |
| **startRow**          | integer | query    | Prima riga da adattare automaticamente (indice in base 1).                                                                           | ✔ |
| **endRow**            | integer | query    | Ultima riga da adattare automaticamente (inclusa).                                                                                   | ✔ |
| **onlyAuto**          | boolean | query    | Se `true`, l'API regola solo le righe la cui altezza viene calcolata automaticamente da Excel. Se `false`, viene eseguito un adattamento completo. | ✖ |
| **folder**            | string  | query    | Cartella contenente il documento.                                                                                                    | ✖ |
| **storageName**       | string  | query    | Nome del servizio di archiviazione.                                                                                                  | ✖ |

Campi di **autoFitterOptions** (tutti opzionali):

- `AutoFitMergedCells` _(boolean)_ – Se `true`, le celle unite vengono prese in considerazione durante il calcolo dell'altezza della riga.
- `IgnoreHidden` _(boolean)_ – Se `true`, le righe nascoste vengono ignorate durante il processo di adattamento automatico.
- `OnlyAuto` _(boolean)_ – Replica il parametro di query `onlyAuto`; quando impostato, sovrascrive il valore del parametro di query.

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Le risposte di errore tipiche includono:

- **400 Bad Request** – Valori dei parametri non validi o corpo JSON malformato.
- **401 Unauthorized** – Token JWT mancante o non valido.
- **404 Not Found** – Il file o il foglio di lavoro specificato non esiste.
- **500 Internal Server Error** – Si è verificato un errore imprevisto sul server.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Bad Request                 | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Unauthorized                | Token JWT non valido o mancante. |
| 413    | Payload Too Large           | Il file caricato supera il limite di dimensione. |
| 500    | Internal Server Error       | Errore imprevisto sul server. |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}