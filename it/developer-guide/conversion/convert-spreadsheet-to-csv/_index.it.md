---
title: "Aspose.Cells Cloud Web API – Convertire Foglio di Lavoro in CSV"
second_title: "Documento"
ArticleTitle: "Come convertire un foglio di lavoro in CSV utilizzando l'API Aspose.Cells Cloud"
linktype: "Converti foglio di lavoro in CSV"
type: docs
url: /convert-spreadsheet-to-csv/
keywords: "Aspose Cells, conversione CSV, API Excel, conversione cloud"
description: "Scopri come convertire file Excel (XLS, XLSX, XLSM, …) in CSV utilizzando l'API Aspose.Cells Cloud. Include i passaggi per l'autenticazione, un esempio cURL, frammenti di codice SDK e gestione degli errori."
weight: 100
---

L'endpoint **ConvertSpreadsheetToCsv** legge un file di foglio di lavoro caricato da un'unità locale, esegue la conversione interamente sui server cloud di Aspose.Cells e restituisce il file CSV risultante come flusso binario. Questa operazione nativa cloud elimina la necessità di caricare il file sorgente nello spazio di archiviazione cloud, riduce i costi di archiviazione e semplifica il flusso di lavoro per gli sviluppatori che necessitano di rapide trasformazioni da foglio di lavoro a CSV. I formati supportati dipendono dalle librerie sottostanti e sono richieste le autorizzazioni appropriate per leggere il file sorgente. Errori come file mancanti, richieste non valide o fallimenti nella conversione vengono restituiti con codici di stato HTTP standard.

## **API Converti foglio di lavoro in CSV**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Posizione | Obbligatorio | Descrizione                                                                                                                                                        |
| :------------- | :----- | :------- | :----------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData | Obbligatorio | Il file di foglio di lavoro da convertire. Accetta formati comuni come .xls, .xlsx, .xlsm. Deve essere fornito come multipart/form‑data. Esempio: `myWorkbook.xlsx`. |
| outPath        | String | Query    | Opzionale    | Percorso della cartella di destinazione in cui salvare il CSV convertito. Se omesso, il CSV viene restituito direttamente nel corpo della risposta. Esempio: `/output/reports/`. |
| outStorageName | String | Query    | Opzionale    | Nome del servizio di archiviazione cloud in cui verrà salvato il file di output. Se non fornito, viene utilizzato lo spazio di archiviazione predefinito configurato per l'account Aspose.Cells. |
| fontsLocation  | String | Query    | Opzionale    | Percorso di una cartella contenente i caratteri personalizzati richiesti dal foglio di lavoro. Abilita il rendering corretto delle celle che utilizzano caratteri non standard. |
| region         | String | Query    | Opzionale    | Impostazione regione/lingua del foglio di lavoro (ad esempio, `it-IT`, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password       | String | Query    | Opzionale    | Password utilizzata per aprire fogli di lavoro protetti da password. Se il file è crittografato e la password è omessa o errata, viene restituito un errore HTTP 400/401. |

### **Risposta**

In caso di esito positivo, l'API restituisce **HTTP 200** (o **202** per l'elaborazione asincrona) con l'intestazione `Content-Type: application/octet-stream`. Il corpo della risposta contiene il file CSV generato come flusso binario.

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

| Codice | Significato              | Descrizione                                                       |
| ------ | ------------------------ | ----------------------------------------------------------------- |
| 200    | OK                       | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida     | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato          | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande    | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Dove dovresti utilizzare l'API Converti foglio di lavoro in CSV?

- **Esportazione dati per sistemi di reporting** – Genera estratti CSV da report basati su Excel per alimentare strumenti BI o data warehouse senza gestire manualmente i file.
- **Elaborazione batch automatizzata** – Converti un gran numero di fogli di lavoro archiviati localmente in CSV all'interno di un processo lato server, quindi invia direttamente i risultati ai servizi a valle.
- **Applicazioni web con caricamento file** – Consenti agli utenti finali di caricare un file Excel e ricevere istantaneamente una versione CSV per ulteriore analisi o importazione in altre piattaforme.
- **Integrazione con sistemi legacy** – Traduci formati legacy di fogli di lavoro in CSV per sistemi che accettano solo file di testo delimitati.

## Perché utilizzare l'API Converti foglio di lavoro in CSV?

- **Architettura senza upload** – Non è necessario memorizzare il file sorgente nello spazio di archiviazione cloud; la conversione avviene direttamente dal flusso caricato, risparmiando tempo e costi di archiviazione.
- **Elaborazione cloud ad alte prestazioni** – Sfrutta il motore di conversione ottimizzato di Aspose.Cells su server cloud scalabili, fornendo output CSV rapidi anche per workbook di grandi dimensioni.
- **Integrazione semplice** – Singola richiesta PUT con parametri di query opzionali; restituisce il CSV come flusso binario pronto per il download, eliminando passaggi di post-elaborazione.
- **Supporto completo delle funzionalità** – Gestisce file protetti da password, caratteri personalizzati e impostazioni locali, garantendo una conversione accurata anche per fogli di lavoro complessi.

## Come utilizzare l'API Converti foglio di lavoro in CSV con gli SDK

### Specifica dell'API Converti foglio di lavoro in CSV

La [Specifiche dell'API Converti foglio di lavoro in CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv) fornisce un'interfaccia di programmazione accessibile pubblicamente per eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello, consentendo di lavorare con i fogli di lavoro utilizzando codice conciso. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud. I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}