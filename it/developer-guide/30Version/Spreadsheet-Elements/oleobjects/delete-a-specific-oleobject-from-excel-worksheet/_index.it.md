---
title: "Eliminare un oggetto OLE in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Elimina"
type: docs
url: /it/oleobjects/delete/
aliases: [/it/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud, Elimina, OLE, Oggetto, Excel, foglio di lavoro, REST, API, SDK"
description: "Scopri come eliminare un oggetto OLE da un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v4.0). Include l'endpoint HTTPS, i passaggi per l'autenticazione, un esempio cURL, frammenti di codice per gli SDK, indicazioni sulla gestione degli errori e link per i passaggi successivi."
weight: 50
ArticleTitle: "Elimina oggetto OLE da foglio di lavoro Excel tramite Aspose.Cells Cloud API"
---

Questa pagina spiega come eliminare un oggetto OLE specifico da un foglio di lavoro in un workbook Excel utilizzando **Aspose.Cells Cloud**. Un oggetto OLE può essere un'immagine collegata, un grafico o qualsiasi oggetto incorporato che Excel memorizza come entità separata.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione tramite token JWT](https://docs.aspose.cloud/it/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### Parametri della richiesta

| Nome parametro   | Tipo    | Posizione | Descrizione                                              |
| ---------------- | ------- | --------- | -------------------------------------------------------- |
| name             | string  | path      | Nome del workbook.                                       |
| sheetName        | string  | path      | Nome del foglio di lavoro.                               |
| oleObjectIndex   | integer | path      | Indice dell'oggetto OLE da eliminare.                    |
| folder           | string  | query     | Cartella contenente il workbook. (opzionale)             |
| storageName      | string  | query     | Nome del servizio di archiviazione. (opzionale)          |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare la chiamata con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
  -X DELETE \
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

### Dettagli della risposta

| Stato HTTP           | Descrizione                                                            | Esempio JSON                                                       |
| -------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------- |
| **200 OK**           | L'oggetto OLE è stato eliminato correttamente.                        | `{ "Code": 200, "Status": "OK" }`                                 |
| **401 Unauthorized** | Token JWT mancante o non valido.                                       | `{ "Code": 401, "Message": "Token di accesso mancante o non valido." }` |
| **404 Not Found**    | Il workbook, il foglio di lavoro o l'indice dell'oggetto OLE specificati non esistono. | `{ "Code": 404, "Message": "Indice dell'oggetto OLE fuori intervallo." }` |
| **400 Bad Request**  | Parametri obbligatori mancanti o non corretti.                        | `{ "Code": 400, "Message": "Parametri della richiesta non validi." }` |

Gestisci queste risposte nella tua applicazione verificando il codice di stato e visualizzando il messaggio associato.

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}