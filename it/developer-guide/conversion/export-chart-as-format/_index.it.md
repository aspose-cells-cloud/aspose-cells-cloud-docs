---
title: "Esporta grafico Excel – API di Aspose.Cells Cloud"
second_title: "Documento"
description: "Converti un grafico da un foglio di calcolo Excel archiviato nel cloud in PDF, PNG, SVG o altri formati con una singola chiamata REST."
ArticleTitle: "Come convertire un foglio di lavoro di un foglio di calcolo locale in un file PDF: Guida passo-passo"
linktitle: "Converti foglio di lavoro in PDF"
type: docs
url: /export-chart-as-format/
keywords: "Aspose.Cells Cloud, esporta grafico, API, PDF, PNG, SVG, Excel, REST, conversione cloud"
weight: 100
---

Converti un grafico presente in un foglio di calcolo archiviato in Aspose Cloud Storage in un formato file diverso (PDF, PNG, SVG, …) senza scaricare il file sorgente.

## API ExportChartAsFormat

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### 📦 Parametri della richiesta

| Nome               | Tipo    | Posizione | Obbligatorio | Descrizione                                                |
| ------------------ | ------- | --------- | ------------ | ---------------------------------------------------------- |
| **name**           | stringa | Percorso  | Sì           | Nome del file del foglio di calcolo.                       |
| **worksheet**      | stringa | Percorso  | Sì           | Nome del foglio di lavoro contenente il grafico.           |
| **chartIndex**     | intero  | Percorso  | Sì           | Indice in base zero del grafico da esportare.              |
| **format**         | stringa | Query     | Sì           | Format di output desiderato (ad es. `png`, `pdf`, `svg`).  |
| **folder**         | stringa | Query     | No           | Percorso della cartella in cui è archiviato il foglio di calcolo (impostazione predefinita: radice). |
| **storageName**    | stringa | Query     | No           | Nome personalizzato dello storage; ometterlo per usare lo storage predefinito. |
| **outPath**        | stringa | Query     | No           | Percorso della cartella in cui verrà salvato il file convertito. |
| **outStorageName** | stringa | Query     | No           | Nome dello storage per il file di output.                  |
| **fontsLocation**  | stringa | Query     | No           | Percorso di una cartella contenente caratteri personalizzati. |
| **region**         | stringa | Query     | No           | Impostazione locale (ad es. `en-US`, `fr-FR`).             |
| **password**       | stringa | Query     | No           | Password per aprire un foglio di calcolo protetto.         |

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                      |
| ------ | --------------------- | ---------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                 |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                |
| 500    | Errore interno del server | Errore imprevisto nel server.                                   |

## Come usare l’API Esporta grafico in un formato con gli SDK?

### Specifica dell’API Esporta grafico in un formato

La [Specifiche dell’API Esporta grafico in un formato](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) fornisce un'interfaccia di programmazione pubblicamente accessibile e consente interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il metodo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendoti di convertire i dati di una tabella di un foglio di calcolo in un file PDF con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK: