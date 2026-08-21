---
title: "Unisci Fogli di Calcolo Corrispondenti in una Cartella Remota"
description: "Unisci file di fogli di calcolo memorizzati nell'archivio cloud di Aspose Cloud in un unico file. Supporta oltre 30 formati di output come PDF, CSV, JSON, XLSX, ODS, XPS e altri."
keywords: "Aspose.Cells, unisci fogli di calcolo, cartella remota, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

Unisci più file di fogli di calcolo memorizzati in una cartella remota dell'archivio cloud di Aspose Cloud in un unico file di output. L'operazione viene eseguita interamente nel cloud, eliminando la necessità di scaricare i file sorgente localmente. Sono supportati oltre 30 formati di output (PDF, CSV, JSON, XLSX, ODS, XPS, …).

## API MergeSpreadsheetsInRemoteFolder

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta <a id="request-parameters"></a>

| Nome                    | Tipo    | Posizione | Obbligatorio | Descrizione                                                                                          |
| ----------------------- | ------- | --------- | ------------ | ---------------------------------------------------------------------------------------------------- |
| **folder**              | string  | query     | **Sì**       | Cartella dell'archivio cloud contenente i fogli di calcolo sorgente.                               |
| **fileMatchExpression** | string  | query     | **Sì**       | Espressione per selezionare i file (es. `*report*.xlsx`). Supporta i caratteri jolly `*` e `?`.     |
| **outFormat**           | string  | query     | **Sì**       | Format di output desiderato (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …).                        |
| **mergeInOneSheet**     | boolean | query     | **Sì**       | `true` – tutti i dati vengono uniti in un'unica cartella di lavoro. `false` – ogni file sorgente ottiene la propria cartella di lavoro. |
| **storageName**         | string  | query     | No           | Nome personalizzato dell'archivio; se omesso, viene utilizzato l'archivio principale.               |
| **outPath**             | string  | query     | No           | Cartella di destinazione per il file unito. Se omesso, il file viene salvato nella cartella sorgente. |
| **outStorageName**      | string  | query     | No           | Nome dell'archivio in cui verrà scritto il file unito.                                              |
| **fontsLocation**       | string  | query     | No           | Percorso di una cartella contenente caratteri personalizzati (necessario per l'esportazione in PDF/immagini). |
| **region**              | string  | query     | No           | Impostazioni locali per la formattazione di numeri, date e valute (es. `it-IT`, `en-US`).           |
| **password**            | string  | query     | No           | Password necessaria per aprire eventuali fogli di calcolo protetti.                                 |

## Esempio di richiesta (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **Risposta**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Il file può essere scaricato direttamente dal campo `FileUrl` oppure salvato nella posizione specificata da `outPath`.

**Dettagli della risposta in caso di successo**

| Codice di stato | Content‑Type               | Descrizione                                         |
| --------------- | -------------------------- | --------------------------------------------------- |
| 200 OK          | `application/octet-stream` | Flusso binario del file del foglio di calcolo unito. |
| 202 Accepted    | `application/json`         | JSON contenente `FileUrl`, `FileName`, ecc.        |

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                   |

## Come utilizzare l'API di unione dei fogli di calcolo con gli SDK

### Specifica OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">Specifica OpenAPI</a> fornisce una descrizione leggibile automaticamente dell'API, consentendo interazioni REST dirette.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file facoltativo"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello e consente di importare dati in una cartella di lavoro con codice breve. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.