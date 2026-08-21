---
title: "Aspose.Cells Cloud – Unisci file Excel nel cloud | Combina fogli di calcolo tramite API"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Unisci file Excel nel cloud – Combina fogli di calcolo online con l'API Aspose.Cells Cloud"
linktitle: "Unisci foglio di calcolo remoto"
type: docs
url: /merge-remote-spreadsheet/
keywords: "Aspose.Cells, unisci Excel, API cloud, combinazione foglio di calcolo"
description: "Unisci cartelle di lavoro Excel archiviate nello storage cloud tramite l'API Aspose.Cells Cloud. Specifica il formato di output, la cartella di destinazione e la modalità di unione in una singola chiamata HTTPS."
weight: 100
---

Unisci rapidamente file Excel archiviati nel cloud con altri fogli di calcolo utilizzando l'API Aspose.Cells Cloud, specificando il formato dei dati di output e la posizione di archiviazione.

## API per l’unione di fogli di calcolo remoti

Prima di chiamare questa operazione, assicurati di disporre di:

- Un **token di accesso JWT** valido (vedi la guida all’autenticazione).
- La cartella di lavoro di origine e tutti i file da unire caricati nello storage cloud.
- Autorizzazioni appropriate per leggere dalla cartella di origine e scrivere nella cartella di destinazione.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione tramite token JWT</a>.

### Parametri della richiesta:

| Nome del parametro | Tipo    | Path/Query String/HTTPBody | Descrizione                                                                                                                          |
| :---------------- | :------ | :------------------------- | :----------------------------------------------------------------------------------------------------------------------------------- |
| name              | String  | Path                       | Nome del file della cartella di lavoro di origine da unire.                                                                        |
| mergedSpreadsheet | String  | Query                      | Elenco separato da virgole dei nomi dei file dei fogli di calcolo da unire nella cartella di lavoro di origine.                     |
| folder            | String  | Query                      | Percorso della cartella nello storage cloud contenente la cartella di lavoro di origine.                                           |
| outFormat         | String  | Query                      | Formato desiderato per il file di output unito (ad esempio, `XLSX`, `PDF`, `CSV`).                                                 |
| mergeInOneSheet   | Boolean | Query                      | Impostato su `true` per unire tutti i dati di origine in un singolo foglio di calcolo; `false` crea fogli separati per ogni file.  |
| storageName       | String  | Query                      | _(Opzionale)_ Nome dello storage cloud in cui si trova la cartella di lavoro di origine. Se omesso, viene utilizzato lo storage predefinito. |
| outPath           | String  | Query                      | _(Opzionale)_ Percorso della cartella di destinazione nello storage cloud per salvare il file unito. Se omesso, il file viene salvato nella cartella di origine. |
| outStorageName    | String  | Query                      | Nome dello storage cloud in cui salvare il file di output.                                                                           |
| fontsLocation     | String  | Query                      | _(Opzionale)_ Percorso personalizzato della cartella per i file di font utilizzati durante la conversione in formati immagine/PDF.   |
| region            | String  | Query                      | _(Opzionale)_ Impostazioni locali/regione per la formattazione di date, numeri e valute nel file di output (ad esempio, `en-US`, `de-DE`). |
| password          | String  | Query                      | _(Opzionale)_ Password necessaria per aprire la cartella di lavoro di origine se protetta.                                          |

### Risposta

**Stato:** `200 OK`

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

Il file può essere scaricato direttamente o salvato nella posizione specificata da `outPath`.

**Dettagli della risposta in caso di successo**

| Codice di stato | Content‑Type               | Descrizione                                |
| --------------- | -------------------------- | ------------------------------------------ |
| 200 OK          | `application/octet-stream` | Flusso binario del file della cartella di lavoro unita. |

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Quando utilizzare l’API per l’unione di fogli di calcolo remoti?

### Integrazione aziendale dei dati

- **Riunione di report interdipartimentali** – Consolidare report Excel separati inviati dai team di vendita, marketing, finanza e altri reparti.
- **Riepilogo dei dati delle filiali** – Raccogliere dati sulle performance di ogni filiale in tutto il mondo.
- **Consolidamento dei dati dei partner** – Unire i dati inviati da più partner in un’unica cartella di lavoro.

### Flusso di lavoro di elaborazione documenti nel cloud

- **Elaborazione dei file nello storage cloud** – Unire direttamente file Excel archiviati in AWS S3, Azure Blob o Google Cloud Storage.
- **Consolidamento dati multi-fonte** – Combinare file provenienti da diverse posizioni cloud in un’unica cartella di lavoro.
- **Pipeline di dati automatizzate** – Integrare l’API nei processi ETL per automatizzare la fusione dei file.

### Automazione della gestione documenti

- **Consolidamento delle versioni** – Unire diverse versioni di un piano di progetto o di una cartella di lavoro di budget.
- **Popolamento dei dati nei modelli** – Inserire file di dati nei modelli standardizzati per la generazione di report.
- **Generazione periodica di report** – Automatizzare i report di sintesi settimanali, mensili e trimestrali.

### Collaborazione cross-platform

- **Collaborazione con team remoti** – Consolidare il lavoro inviato da membri del team distribuiti in diverse sedi.
- **Organizzazione dei dati dei clienti** – Unire dati sugli ordini o sui feedback provenienti da più clienti.
- **Riepilogo delle informazioni dei fornitori** – Combinare preventivi o informazioni sui prodotti di diversi fornitori.

## Perché utilizzare l’API per l’unione di fogli di calcolo remoti?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud fornisce SDK per molti linguaggi, riducendo i tempi di sviluppo e offrendo documentazione completa. Rispetto alla creazione di una soluzione personalizzata, questo riduce notevolmente il carico di lavoro.
- **Riduzione dei costi del personale** – Diminuisce la necessità di personale dedicato alla fusione manuale dei documenti.
- **Pagamento in base all’uso** – Nessun investimento iniziale: si paga solo per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione nulli** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare l’API per l’unione di fogli di calcolo remoti con gli SDK

### Specifica dell’API per l’unione di fogli di calcolo remoti

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">specifiche dell’API per l’unione di fogli di calcolo remoti</a> descrive l’interfaccia REST che può essere chiamata direttamente da qualsiasi client HTTP.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells Cloud. Il seguente esempio mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
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

### Utilizzare gli SDK Aspose.Cells Cloud

L’utilizzo di un SDK rappresenta il metodo più rapido per lo sviluppo, poiché astrae i dettagli a basso livello e consente di unire un foglio di calcolo in un altro tramite un breve frammento di codice.  
Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per l’elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come interagire con i servizi web Aspose.Cells Cloud utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}