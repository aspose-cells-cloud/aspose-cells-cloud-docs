---
title: "Unisci più file Excel in un unico foglio di calcolo – Aspose.Cells Cloud API"
second_title: "Documenti"
ArticleTitle: "Combina più file Excel in uno – Unisci in batch fogli di calcolo in oltre 30 formati"
linktype: "Unisci fogli di calcolo"
type: docs
url: /merge-spreadsheets/
keywords: "Aspose.Cells, unisci fogli di calcolo, Excel API, foglio di calcolo cloud, unione in batch, conversione in PDF, unione CSV, unione ODS, riferimento API, SDK"
description: "Unisci più file locali Excel, CSV o ODS in un unico workbook e converti il risultato in oltre 30 formati (PDF, HTML, ecc.) con Aspose.Cells Cloud. Include endpoint, parametri, guida all'autenticazione ed esempi di SDK."
weight: 100
---

Unisci più file locali Excel, CSV o ODS in un unico workbook e convertilo in oltre 30 formati di output con l’API Aspose.Cells Cloud.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione         | Descrizione                                                                                      |
| --------------- | ------- | ---------------- | ------------------------------------------------------------------------------------------------ |
| Spreadsheet     | File    | FormData         | Il file locale del foglio di calcolo da caricare. Supporta XLSX, XLS, CSV, ODS, ecc.            |
| outFormat       | String  | Query            | Format di output desiderato (ad esempio, `XLSX`, `PDF`, `CSV`, `HTML`). Supporta oltre 30 formati. |
| mergeInOneSheet | Boolean | Query            | `true` → tutti i dati uniti in un'unica foglio; `false` → ogni foglio originale viene preservato. |
| outPath         | String  | Query (opzionale) | Percorso della cartella cloud in cui salvare il file unito. Se omesso, viene usata la posizione predefinita. |
| outStorageName  | String  | Query            | Nome dello storage cloud da utilizzare (predefinito o personalizzato).                           |
| fontsLocation   | String  | Query (opzionale) | Cartella cloud contenente i caratteri personalizzati per il rendering corretto di PDF e immagini. |
| region          | String  | Query (opzionale) | Impostazioni locali per la formattazione di numeri, date e valute (ad esempio, `en-US`, `zh-CN`). |
| password        | String  | Query (opzionale) | Password per aprire un foglio di calcolo protetto.                                              |

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

Il file può essere scaricato direttamente o salvato nella posizione specificata da `outPath`.

**Dettagli della risposta in caso di successo**

| Codice di stato | Content‑Type               | Descrizione                                |
| --------------- | -------------------------- | ------------------------------------------ |
| 200 OK          | `application/octet-stream` | Flusso binario del file workbook unito.    |

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | File caricato supera il limite di dimensione.                     |
| 500    | Errore interno del server | Errore imprevisto del server.                                       |

## Dove utilizzare l’API di unione di fogli di calcolo?

### **Istruzione e applicazioni accademiche**

- **Valutazione dei compiti degli studenti** – Unisci più file di compiti degli studenti per commenti e valutazioni unificati.
- **Raccolta dati per la ricerca** – Consolida fogli di calcolo di dati provenienti da diversi gruppi sperimentali.
- **Creazione di materiali didattici** – Unisci esercizi provenienti da diversi capitoli in un unico workbook per un banco di domande.

### **Elaborazione e analisi dei dati**

- **Integrazione di piccoli set di dati** – Unisci file CSV o Excel esportati da fonti diverse.
- **Pre-elaborazione per l’analisi dei dati** – Unisci file di dati rilevanti prima di effettuare l’analisi.
- **Compilazione di modelli di report** – Popola modelli di report predefiniti con dati uniti.

### **Sviluppo e supporto tecnico**

- **Preparazione di dati per i test** – Unisci più file di casi di test per i test automatizzati.
- **Analisi dei file di log** – Consolida report Excel dei log di sistema provenienti da periodi diversi.
- **Gestione della configurazione** – Unisci più fogli di calcolo di configurazione in un unico file di configurazione.

## Perché utilizzare l’API di unione di fogli di calcolo?

- **Facile da usare per gli sviluppatori** – Le librerie SDK sono disponibili per molti linguaggi, riducendo lo sforzo di sviluppo rispetto alla creazione di una soluzione personalizzata.
- **Riduzione dei costi del personale** – Elimina la necessità di personale dedicato per la consolidazione manuale dei documenti.
- **Pagamento in base all’uso** – Paghi solo per le chiamate API effettivamente effettuate; nessun investimento iniziale.
- **Costi di manutenzione nulli** – Nessun server da gestire, nessun aggiornamento software, nessun problema di compatibilità.

## Come utilizzare l’API di unione di fogli di calcolo con gli SDK

### Specifica OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">Specifica OpenAPI</a> fornisce una descrizione leggibile automaticamente dell’API, consentendo interazioni REST dirette.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
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

L'utilizzo degli SDK rappresenta il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello e consente di importare dati in un foglio di calcolo con poche righe di codice. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}