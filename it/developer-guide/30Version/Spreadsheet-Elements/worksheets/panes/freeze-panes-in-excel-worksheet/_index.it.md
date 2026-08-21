---
title: "Blocca i riquadri in un foglio di Excel"
second_title: "Documento"
linktype: "Blocca"
type: docs
url: /it/worksheets/panes/freeze/
aliases: [  /it/freeze-panes-in-excel-worksheet/ , /it/worksheets/freeze-panes/ ]
keywords: "Aspose.Cells Cloud, blocco riquadri, Excel, REST API, foglio di lavoro"
description: "Scopri come bloccare righe e colonne in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi dell'endpoint, i parametri obbligatori, un esempio cURL, istruzioni per l'autenticazione, dettagli sulle risposte di errore e codici di esempio per SDK in diversi linguaggi."
weight: 190
---

Questa API REST **imposta** il blocco dei riquadri in un foglio di lavoro Excel.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

I parametri della richiesta sono:

| Nome parametro | Tipo    | Posizione | Descrizione                                              |
| -------------- | ------- | --------- | -------------------------------------------------------- |
| name           | string  | path      | Nome del file del foglio di calcolo.                    |
| sheetName      | string  | path      | Nome del foglio di lavoro in cui bloccare i riquadri.   |
| row            | integer | query     | Indice in base zero della prima riga **non bloccata**.  |
| column         | integer | query     | Indice in base zero della prima colonna **non bloccata**. |
| frozenRows     | integer | query     | Numero di righe da bloccare a partire dall'alto.        |
| frozenColumns  | integer | query     | Numero di colonne da bloccare a partire da sinistra.    |
| folder         | string  | query     | Percorso della cartella nella memoria in cui risiede il foglio di calcolo. |
| storageName    | string  | query     | Nome del servizio di archiviazione.                      |

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### Risposta di errore

| Stato HTTP                | Codice | Messaggio                          | Esempio                                                  |
| ------------------------- | ------ | ---------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400    | Parametri non validi               | `{ "Code": 400, "Message": "Valore di frozenRows non valido" }` |
| 401 Unauthorized          | 401    | Token JWT mancante o non valido     | `{ "Code": 401, "Message": "Token di accesso non valido" }` |
| 404 Not Found             | 404    | Foglio di calcolo o foglio di lavoro non trovato | `{ "Code": 404, "Message": "File non trovato" }` |
| 500 Internal Server Error | 500    | Errore imprevisto del server       | `{ "Code": 500, "Message": "Errore interno del server" }` |

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}