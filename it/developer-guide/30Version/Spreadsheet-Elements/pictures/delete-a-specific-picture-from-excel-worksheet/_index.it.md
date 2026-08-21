---
title: "Eliminare un'immagine da un foglio di lavoro Excel – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Elimina"
type: docs
url: /it/pictures/delete/
aliases: [  /it/delete-a-specific-picture-from-excel-worksheet/ ]
keywords: "Aspose.Cells, Cloud API, elimina immagine, foglio di lavoro Excel, REST"
description: "Elimina un'immagine da un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Scopri l'endpoint DELETE, i parametri richiesti, l'autenticazione, i codici di errore e il codice di esempio."
weight: 50
ArticleTitle: "Eliminare un'immagine da un foglio di lavoro Excel – Aspose.Cells Cloud API"
---

Questa API REST elimina un'immagine da un foglio di lavoro Excel.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione | Obbligatorio | Descrizione                                           |
| -------------- | ------- | --------- | ------------ | ----------------------------------------------------- |
| name           | string  | path      | Sì           | Nome del file del workbook.                          |
| sheetName      | string  | path      | Sì           | Nome del foglio di lavoro contenente l'immagine.    |
| pictureIndex   | integer | path      | Sì           | Indice in base zero dell'immagine da eliminare.     |
| folder         | string  | query     | No           | Cartella in cui è memorizzato il workbook.          |
| storageName    | string  | query     | No           | Nome del servizio di archiviazione (opzionale).     |

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare la chiamata con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**Intestazioni di esempio della risposta**

| Intestazione    | Valore                        |
|----------------|------------------------------|
| Content-Type   | application/json             |
| Content-Length | (varia)                      |
| Date           | (data del server)            |

{{< /tab >}}

{{< /tabs >}}

### Gestione degli errori

| Codice HTTP | Significato                                                       | Payload di errore di esempio                                          |
|-------------|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| 200         | Immagine eliminata con successo.                                 | `{ "Code": 200, "Status": "OK" }`                                     |
| 400         | Richiesta non valida – parametri non corretti.                   | `{ "Code": 400, "Message": "pictureIndex non valido." }`             |
| 401         | Non autorizzato – token mancante o non valido.                   | `{ "Code": 401, "Message": "Token di accesso mancante o non valido." }` |
| 404         | Non trovato – il workbook, il foglio di lavoro o l'immagine non esistono. | `{ "Code": 404, "Message": "Risorsa non trovata." }`                 |
| 500         | Errore interno del server.                                       | `{ "Code": 500, "Message": "Errore imprevisto del server." }`        |

## Famiglia di SDK per il Cloud

L'uso di un SDK rappresenta il metodo più rapido per lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}