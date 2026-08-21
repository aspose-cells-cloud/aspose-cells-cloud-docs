---
title: "Elimina area celle – Documentazione API di Aspose.Cells Cloud"
type: docs
url: /it/conditional-formattings/delete-cell-area/
aliases: [  /it/remove-cell-area-from-conditional-formatting/ ]
keywords: "Aspose.Cells Cloud, Elimina area celle, API formattazione condizionale, API REST Excel"
description: "Utilizza l'API REST di Aspose.Cells Cloud per eliminare un'area di celle specifica da una regola di formattazione condizionale in un foglio di calcolo Excel. Include esempi in ASP.NET, Java e Python."
ArticleTitle: "Elimina area celle – Documentazione API di Aspose.Cells Cloud"
weight: 70
---

Questa API REST elimina un'area di celle da una regola di formattazione condizionale.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                           |
| -------------- | ------- | --------- | --------------------------------------------------------------------- |
| `name`         | string  | path      | Nome del file Excel.                                                  |
| `sheetName`    | string  | path      | Nome del foglio di calcolo contenente la formattazione condizionale. |
| `startRow`     | integer | query     | Indice in base zero della prima riga dell’area da rimuovere.        |
| `startColumn`  | integer | query     | Indice in base zero della prima colonna dell’area da rimuovere.     |
| `totalRows`    | integer | query     | Numero di righe nell’area da rimuovere.                             |
| `totalColumns` | integer | query     | Numero di colonne nell’area da rimuovere.                           |
| `folder`       | string  | query     | Cartella nell’archivio cloud in cui si trova il file (opzionale).    |
| `storageName`  | string  | query     | Nome del servizio di archiviazione (opzionale).                      |

### Risposte di errore

| Stato HTTP | Codice          | Descrizione                                                | JSON di esempio                                                    |
| ---------- | --------------- | ---------------------------------------------------------- | ------------------------------------------------------------------ |
| 400        | `BadRequest`    | Parametri mancanti o non validi.                           | `{ "Code": "400", "Message": "Parametri della richiesta non validi." }` |
| 401        | `Unauthorized`  | Token JWT mancante o non valido.                           | `{ "Code": "401", "Message": "Autenticazione non riuscita." }`     |
| 404        | `NotFound`      | File, foglio di calcolo o formattazione condizionale non trovati. | `{ "Code": "404", "Message": "Risorsa non trovata." }`             |
| 500        | `InternalError` | Errore imprevisto del server.                              | `{ "Code": "500", "Message": "Errore interno del server." }`       |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi di Aspose.Cells Cloud. L'esempio seguente mostra come chiamare l'endpoint **Elimina area celle** con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}
---