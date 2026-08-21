---
title: "Elimina tutte le immagini in un foglio di lavoro di Excel"
second_title: "Documento"
linktitle: "Cancella"
type: docs
url: /it/pictures/clear/
aliases: [  /it/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, elimina tutte le immagini, foglio di lavoro, REST API, cancella immagini"
description: "Scopri come eliminare tutte le immagini da un foglio di lavoro di Excel utilizzando l'API REST di Aspose.Cells Cloud con esempi in cURL e SDK."
weight: 60
ArticleTitle: "Come eliminare tutte le immagini in un foglio di lavoro di Excel con Aspose.Cells Cloud"
---

Questa REST API elimina **tutte** le immagini presenti in un foglio di lavoro.

**Prerequisiti**  
- Un account Aspose.Cells Cloud attivo con un token di accesso OAuth 2.0 valido.  
- È richiesta la versione 3.0 (o successiva) dell'API; le versioni precedenti sono deprecate.  
- Il file Excel di destinazione deve essere memorizzato in una posizione di archiviazione supportata (predefinita o personalizzata).

**Compatibilità con le versioni**  
L'endpoint segue la specifica dell'API Cells Cloud 3.0. Assicurati che le tue librerie client e gli URL delle richieste puntino a `api.aspose.cloud/v3.0`.

## API DeleteWorksheetPictures

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                   |
| -------------- | ------ | --------- | --------------------------------------------- |
| name           | string | Path      | Nome del file Excel.                          |
| sheetName      | string | Path      | Nome del foglio di lavoro contenente le immagini. |
| folder         | string | Query     | Cartella in cui è memorizzato il file.        |
| storageName    | string | Query     | Nome del servizio di archiviazione.           |

### Risposte di errore

| Codice HTTP | Descrizione                                                                    |
| ----------- | ------------------------------------------------------------------------------ |
| 401         | Non autorizzato – token mancante o non valido.                                |
| 404         | Non trovato – il file, il foglio di lavoro o l'indice di interruzione di pagina specificato non esiste. |
| 400         | Richiesta non valida – sintassi della richiesta errata o parametri non validi. |
| 500         | Errore interno del server – si è verificata una condizione imprevista.        |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
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

## Famiglia di SDK per il Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulla logica aziendale. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Note:** L'operazione DELETE non supporta la paginazione ed è soggetta ai limiti di frequenza standard delle API di Aspose.Cells Cloud (predefiniti: 100 richieste al minuto). Adatta di conseguenza la logica del tuo client.

**Vedi anche**:  
- [/pictures/delete/](../delete/) – Elimina un’immagine specifica da un foglio di lavoro.  
- [/pictures/add/](../add/) – Aggiungi un’immagine a un foglio di lavoro.  
---