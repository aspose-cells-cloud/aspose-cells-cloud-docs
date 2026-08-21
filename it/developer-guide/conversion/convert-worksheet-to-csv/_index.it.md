---
title: "Convertire Foglio di Lavoro in CSV – Documentazione API Aspose.Cells Cloud"
second_title: "Documenti"
ArticleTitle: "Come Convertire un Foglio di Calcolo in CSV Utilizzando l'API Aspose.Cells Cloud"
linktitle: "Convertire Foglio di Lavoro in CSV"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, conversione CSV, foglio di lavoro in CSV, API REST, foglio di calcolo cloud, Excel in CSV"
description: "Scopri come convertire un foglio di lavoro specifico da un file Excel in CSV utilizzando l'API Aspose.Cells Cloud (v4.0). Include endpoint, parametri, esempi cURL, codice SDK e gestione degli errori."
weight: 100
---

L'endpoint **ConvertWorksheetToCsv** trasforma un singolo foglio di lavoro da un file di foglio di calcolo locale in un documento CSV interamente sul server Aspose.Cells Cloud. Caricando il file sorgente e specificando il foglio di lavoro di destinazione, gli sviluppatori ricevono un flusso binario CSV senza dover salvare il file nello storage cloud. Questa API è ideale per automatizzare l'estrazione dei dati, integrare dati da fogli di calcolo in sistemi downstream e ridurre i costi di archiviazione.

## API per la Conversione del Foglio di Lavoro in CSV

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **Sicurezza e Autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della Richiesta

| Nome Parametro | Tipo   | Posizione | Obbligatorio/Opzionale | Descrizione                                                                                                                                 |
| :------------- | :----- | :------- | :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | File   | FormData | **Obbligatorio**       | File binario del foglio di calcolo sorgente (ad es. `.xlsx`, `.xls`). Esempio: `myWorkbook.xlsx`.                                            |
| worksheet      | String | Query    | **Obbligatorio**       | Nome del foglio di lavoro da convertire (case-sensitive). Se omesso, viene utilizzato il primo foglio. Esempio: `Sheet1`.                    |
| outPath        | String | Query    | Opzionale              | Percorso della cartella di destinazione nello storage cloud dove salvare il CSV generato. Se omesso, il CSV viene restituito direttamente nel flusso di risposta. |
| outStorageName | String | Query    | Opzionale              | Nome del servizio di storage (ad es. Azure, AWS S3) in cui posizionare il file di output. Obbligatorio solo se viene utilizzato `outPath`.   |
| fontsLocation  | String | Query    | Opzionale              | Percorso di una cartella personalizzata dei font sul server, consentendo al motore di conversione di utilizzare font non standard.          |
| region         | String | Query    | Opzionale              | Identificatore di localizzazione che influisce sul formato di numeri/date nel CSV (ad es. `it-IT`, `en-US`, `fr-FR`).                      |
| password       | String | Query    | Opzionale              | Password per aprire un foglio di calcolo protetto. Deve corrispondere alla password di crittografia del file sorgente.                      |

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

**Codici di Stato HTTP**

| Codice | Significato            | Descrizione                                                      |
| ------ | ---------------------- | ---------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Non Validata | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non Autorizzato        | Token JWT non valido o mancante.                                 |
| 413    | Payload Troppo Grande  | Il file caricato supera il limite di dimensione.                |
| 500    | Errore Interno del Server | Errore imprevisto sul server.                                   |

## Quando Utilizzare l'API per la Conversione del Foglio di Lavoro in CSV?

- **Estrazione Dati per Pipeline BI** – Recuperare un foglio di lavoro specifico da un report Excel e inviare direttamente il CSV risultante a Power BI o Tableau, senza gestire file intermedi.
- **Elaborazione Automatica Fatture** – Convertire in CSV il foglio di lavoro contenente le righe fattura per un rapido import in sistemi contabili.
- **Integrazione con Sistemi Legacy** – Esportare dati da fogli di lavoro in CSV per l'utilizzo da parte di applicazioni più datate che accettano solo file di testo delimitati.
- **Generazione di Report in Tempo Reale** – Produrre istantanee CSV dei dati di fogli di calcolo live in un servizio web, restituendo il file istantaneamente al browser del client.

## Perché Utilizzare l'API per la Conversione del Foglio di Lavoro in CSV?

- **Nessuno storage cloud permanente richiesto** – Il file viene inviato direttamente al motore di conversione e scartato dopo la conversione, risparmiando larghezza di banda e costi di archiviazione.
- **Esecuzione su Cloud ad Alto Rendimento** – La conversione avviene sui server ottimizzati di Aspose, completandosi tipicamente entro 2 secondi per file fino a 100 MB.
- **Controllo Granulare** – Selezionare un singolo foglio di lavoro, applicare font personalizzati, formattazione regionale e protezione tramite password in una sola richiesta.
- **Output CSV Consistente su Piattaforme Diverse** – Garantisce output CSV identici su .NET, Java, Python e altri SDK che utilizzano lo stesso endpoint REST.

## Come Usare l'API per la Conversione del Foglio di Lavoro in CSV con gli SDK

### Specifica dell'API per la Conversione del Foglio di Lavoro in CSV

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">Specifica dell'API per la Conversione del Foglio di Lavoro in CSV</a> fornisce un'interfaccia di programmazione pubblicamente accessibile per eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK semplifica lo sviluppo astrattendo i dettagli di basso livello, consentendo di unire un foglio di calcolo in un altro con codice conciso. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come interagire con i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}