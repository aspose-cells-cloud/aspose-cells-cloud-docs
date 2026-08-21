---
---
title: "Aspose.Cells Cloud Web API – Convertire un foglio di lavoro in HTML"
second_title: "Documento"
ArticleTitle: "Come convertire un foglio di lavoro in HTML utilizzando l'API Aspose.Cells Cloud"
linktitle: "Convertire foglio di lavoro in HTML"
type: docs
url: /convert-worksheet-to-html/
description: "Scopri come convertire un foglio di lavoro Excel in HTML utilizzando l'API Aspose.Cells Cloud: nessun caricamento richiesto, font personalizzati, supporto per le impostazioni locali e gestione degli errori."
keywords: "Aspose.Cells, Excel in HTML, conversione foglio di lavoro, API cloud"
weight: 100
---

L'endpoint **ConvertWorksheetToHtml** legge un file Excel dal file system locale, estrae il foglio di lavoro specificato e restituisce il contenuto come file HTML. La conversione viene eseguita interamente sui server cloud di Aspose, quindi non è richiesto alcun caricamento o archiviazione intermedi. Ideale per generare visualizzazioni pronte per il web dei dati di fogli di calcolo, l'API supporta percorsi di output opzionali, font personalizzati, impostazioni locali e cartelle di lavoro protette da password.

## API per la conversione di un foglio di lavoro in HTML

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Obbligatorio/opzionale | Descrizione                                                                                                                                                                                                 |
| :------------- | :----- | :------- | :--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | Obbligatorio | FormData             | File Excel binario da elaborare. Deve essere un file .xlsx, .xls, .xlsb, ecc. valido. Esempio: `myWorkbook.xlsx`. Il file Excel viene letto direttamente dal corpo della richiesta; non è necessario caricarlo preventivamente nello storage cloud. |
| worksheet      | String | Obbligatorio | Query                | Nome del foglio di lavoro da convertire (distinzione tra maiuscole e minuscole). Deve esistere nella cartella di lavoro fornita. Esempio: `Sheet1`.                                                       |
| outPath        | String | Opzionale    | Query                | Percorso della cartella di destinazione (nello storage cloud) dove verrà salvato il file HTML generato. Se omesso, il file viene restituito direttamente nella risposta. Esempio: `/output/html/`.             |
| outStorageName | String | Opzionale    | Query                | Nome del servizio di storage cloud da utilizzare per `outPath`. Richiesto solo quando `outPath` punta a uno storage non predefinito.                                                                        |
| fontsLocation  | String | Opzionale    | Query                | Percorso assoluto a una cartella contenente font TrueType/OpenType personalizzati da utilizzare durante la conversione. Permette un rendering corretto dei caratteri non standard.                             |
| region         | String | Opzionale    | Query                | Identificatore di localizzazione che influenza il formato di numeri e date (ad esempio, `it-IT`, `en-US`, `fr-FR`). Di default assume l'impostazione interna della cartella di lavoro.                          |
| password       | String | Opzionale    | Query                | Password necessaria per aprire una cartella di lavoro protetta. Omessa per file non protetti.                                                                                                               |

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

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto nel server.                                     |

## Dove dovremmo utilizzare l'API per la conversione di un foglio di lavoro in HTML?

- Inserire dati di fogli di calcolo live in un portale web – Convertire un foglio di lavoro di report finanziari in HTML per la visualizzazione diretta nei browser senza richiedere plugin Excel.
- Generare fatture HTML stampabili da un modello Excel – Automatizzare la creazione di pagine fattura pronte per il web a partire da un foglio di lavoro predefinito.
- Creare frammenti di documentazione – Convertire fogli di specifiche di progettazione in frammenti HTML da inserire in manuali tecnici o wiki.
- Sviluppare dashboard BI a basso codice – Estrarre dati da un foglio di lavoro, convertirli in HTML e visualizzarli all'interno di widget di dashboard personalizzati.

## Perché utilizzare l'API per la conversione di un foglio di lavoro in HTML?

- **Flusso di lavoro senza caricamento** – Convertire file locali direttamente nel cloud, eliminando la necessità di trasferire preventivamente grandi cartelle di lavoro allo storage.
- **Rendering ad alte prestazioni** – La conversione lato server sfrutta il motore ottimizzato di Aspose, fornendo output HTML veloci e accurati.
- **Controllo completo sull'output** – I parametri opzionali (font personalizzati, area geografica, password) permettono di adattare l'HTML alle esigenze locali e di branding.
- **Integrazione fluida** – Una semplice richiesta PUT con `multipart/form-data` si integra naturalmente in pipeline CI/CD, microservizi o funzioni serverless.

## Come utilizzare l'API per la conversione di un foglio di lavoro in HTML con gli SDK

### Specifica dell'API per la conversione di un foglio di lavoro in HTML

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">Specifica dell'API Convert Worksheet to HTML</a> fornisce un'interfaccia di programmazione accessibile pubblicamente per eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendo di unire fogli di lavoro con codice conciso.  
Consultare il <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">repository GitHub degli SDK di Aspose.Cells Cloud</a> per un elenco completo degli SDK disponibili.  
I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}