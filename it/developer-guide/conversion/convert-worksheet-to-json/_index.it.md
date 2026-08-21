---
---
title: "Aspose.Cells Cloud Web API – Converti foglio di calcolo in JSON"
second_title: "Documento"
ArticleTitle: "Come convertire un foglio di calcolo in JSON utilizzando l'API Aspose.Cells Cloud"
linktitle: "Converti foglio di calcolo in JSON"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, foglio di calcolo in JSON, conversione Excel, API cloud, API v4, esportazione dati"
description: "Guida passo passo per convertire un foglio di calcolo Excel in JSON tramite l'API Aspose.Cells Cloud, inclusi parametri di richiesta, gestione della risposta, codici di errore ed esempi di SDK."
weight: 100
---

L'endpoint **ConvertWorksheetToJson** legge un file di foglio di calcolo dal file system locale, estrae il foglio specificato e restituisce il relativo contenuto come file JSON. La conversione avviene interamente sui server Aspose.Cells Cloud, pertanto non è necessario alcun caricamento o archiviazione intermedio. Supporta cartelle di lavoro protette da password, percorsi personalizzati dei caratteri e impostazioni internazionali, offrendo una soluzione rapida e nativa nel cloud per esportare i dati del foglio in JSON per l'elaborazione successiva.

## **API Converti foglio di calcolo in JSON**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Posizione | Obbligatorio/Opzionale | Descrizione                                                                                                                                                                                         |
| :------------- | :----- | :-------- | :--------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | file   | FormData  | Obbligatorio           | La cartella di lavoro Excel da elaborare. Deve essere in un formato supportato (xls, xlsx, csv, ecc.). Inviata come multipart/form-data. Esempio: `Spreadsheet=@C:\Docs\Sample.xlsx`.                   |
| worksheet      | string | Query     | Obbligatorio           | Nome esatto del foglio da convertire (distinzione maiuscole/minuscole). Se omesso o non trovato, l'API restituisce un errore. Esempio: `worksheet=Sheet1`.                                            |
| outPath        | string | Query     | Opzionale              | Cartella di destinazione nello storage cloud configurato in cui verrà salvato il file JSON generato. Se non fornito, il JSON viene restituito direttamente nel flusso di risposta. Esempio: `outPath=/converted/`. |
| outStorageName | string | Query     | Opzionale              | Nome dello storage di destinazione (es. "MyStorage") che contiene `outPath`. Viene utilizzato lo storage predefinito se omesso.                                                                      |
| fontsLocation  | string | Query     | Opzionale              | Cartella lato server che contiene i caratteri personalizzati necessari per il rendering accurato del testo nel foglio. Esempio: `fontsLocation=/fonts/custom/`.                                       |
| region         | string | Query     | Opzionale              | Identificatore culturale/internazionale che influenza la formattazione di numeri, date e valute nel JSON generato (es. `it-IT`, `fr-FR`).                                                           |
| password       | string | Query     | Opzionale              | Password per aprire una cartella di lavoro crittografata. Se la cartella di lavoro non è protetta da password, omettere questo parametro.                                                          |

### **Risposta**

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

| Codice | Significato             | Descrizione                                                        |
| ------ | ----------------------- | ------------------------------------------------------------------ |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                   |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto sul server.                                      |

## Dove utilizzare l'API Converti foglio di calcolo in JSON?

- **Dashboard web** – Esporta i dati del foglio in JSON per librerie di grafica lato client (es. Chart.js, D3.js).
- **Migrazione dati** – Trasferisci dati Excel legacy in database NoSQL o servizi REST che accettano input JSON.
- **App mobili o offline** – Converti il contenuto del foglio in JSON sul server, quindi sincronizza il payload leggero sui dispositivi mobili.
- **Pipeline di reportistica** – Fornisci direttamente i dati del foglio a motori di analisi che accettano input JSON, senza passaggi intermedi in CSV.

## Perché utilizzare l'API Converti foglio di calcolo in JSON?

- **Flusso di lavoro senza caricamento** – Elabora file locali nel cloud senza caricarli preventivamente nello storage, risparmiando larghezza di banda e costi di archiviazione.
- **Conversione completa** – Supporta cartelle di lavoro protette da password, caratteri personalizzati e formattazione internazionale per una rappresentazione accurata dei dati.
- **Esecuzione rapida e scalabile** – Sfrutta il motore ad alte prestazioni Aspose.Cells su infrastruttura cloud, gestendo in modo efficiente fogli di calcolo di grandi dimensioni.
- **Integrazione semplificata** – Una singola chiamata PUT restituisce un file JSON pronto all’uso o lo memorizza direttamente, riducendo la complessità del codice nelle applicazioni client.

## Come utilizzare l'API Converti foglio di calcolo in JSON con gli SDK

### Specifica dell'API Converti foglio di calcolo in JSON

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">Specifiche dell'API Converti foglio di calcolo in JSON</a> fornisce un'interfaccia di programmazione accessibile pubblicamente per eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

L'utilizzo degli SDK rappresenta il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello e consente di lavorare con i fogli di calcolo tramite codice conciso. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.  
I seguenti esempi di codice mostrano come interagire con i servizi web Aspose.Cells tramite vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}