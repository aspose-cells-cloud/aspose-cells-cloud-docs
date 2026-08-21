---
---
title: "Aspose.Cells Cloud Data Import API – Una soluzione cloud per l'importazione automatica di dati CSV, JSON e XML in fogli di calcolo Excel."
second_title: "Documento"
ArticleTitle: "Piattaforma di integrazione dati multi-fonte per Excel – Aspose.Cells Cloud API per l'importazione e la trasformazione automatica dei dati."
linktitle: "Importa dati in un foglio di calcolo"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Aspose Cells, API per l'importazione dati, CSV in Excel, JSON in Excel, XML in Excel, foglio di calcolo cloud, API REST"
description: "Importa dati CSV, JSON o XML nei fogli di calcolo Excel tramite l'API REST di Aspose.Cells Cloud. Scopri il formato della richiesta, i parametri, il codice di esempio con SDK e la gestione degli errori."
weight: 100
---

## Caratteristiche principali

### Supporto per dati in diversi formati

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">Importazione dati CSV</a>**: supporta diversi delimitatori e rileva automaticamente la codifica.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">Gestione dati JSON</a>**: appiattisce strutture JSON complesse in tabelle Excel.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Conversione file XML</a>**: mappa i dati dei nodi alla struttura riga e colonna di Excel.

## **Descrizione dell’API Import Data into Spreadsheet**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro     | Tipo   | Posizione         | Descrizione                                                                 |
| ------------------ | ------ | ----------------- | --------------------------------------------------------------------------- |
| datafile           | File   | FormData          | Il file di dati (CSV, JSON o XML) da importare.                            |
| spreadsheet        | File   | FormData          | Il workbook di destinazione che riceverà i dati importati.                 |
| worksheet          | string | Query             | Nome del foglio di calcolo in cui verranno posizionati i dati.             |
| startCell          | string | Query             | Cella in alto a sinistra (es. `A1`) che indica la posizione iniziale.      |
| insert             | bool   | Query             | `true` per inserire righe; `false` per sovrascrivere i dati esistenti.     |
| convertNumericData | bool   | Query             | `true` per convertire stringhe numeriche in numeri durante l’importazione. |
| splitter           | string | Query             | Delimitatore CSV a singolo carattere (il valore predefinito è `,`).        |
| outPath            | string | Query (opzionale) | Percorso della cartella in cui verrà salvato il workbook aggiornato.       |
| outStorageName     | string | Query (opzionale) | Nome della posizione di archiviazione per il file di output.                |
| fontsLocation      | string | Query (opzionale) | Percorso di una cartella di caratteri personalizzata, se necessario.       |
| region             | string | Query (opzionale) | Configurazione regionale del foglio di calcolo (es. `it-IT`).              |
| password           | string | Query (opzionale) | Password per aprire un workbook protetto.                                  |

### Risposta

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                    |
| ------ | ----------------------- | -------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                               |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.               |
| 500    | Errore interno del server | Errore imprevisto sul server.                                  |

## Perché utilizzare questa API

- **Caricamento dati efficiente** – Consente l’importazione in blocco di grandi set di dati direttamente in un workbook, senza creare file intermedi.
- **Ampio supporto per gli SDK** – Fornisce librerie client per .NET, Java, PHP, Ruby, Node.js, Python, Go e Perl, semplificando l’integrazione.
- **Elaborazione in memoria** – Esegue le trasformazioni in memoria, riducendo i requisiti di archiviazione temporanea.

## Come utilizzare l’API Import Data into Spreadsheet con gli SDK

**Note / Limitazioni:** L’API supporta fino a 1 000 000 di righe per importazione. Come delimitatore CSV predefinito è utilizzata solo la virgola; altri delimitatori a singolo carattere possono essere specificati tramite il parametro `splitter`. File XML di grandi dimensioni possono aumentare il tempo di elaborazione.

Per operazioni correlate, come l’esportazione dei dati o la conversione dei formati dei workbook, consulta la documentazione **Esportazione dati** e **Conversione workbook**.

### Specifica dell’API Import Data into Spreadsheet

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">Specifica dell’API Import Data into Spreadsheet</a> fornisce un’interfaccia di programmazione accessibile pubblicamente, consentendo interazioni REST direttamente dal tuo browser web.
Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
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

L’utilizzo dell’SDK rappresenta il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendoti di importare dati in un foglio di calcolo con poche righe di codice. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.