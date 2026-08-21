---
title: "Aspose.Cells Cloud Web API – Convertire foglio di calcolo in PDF"
second_title: "Documento"
ArticleTitle: "Come convertire un foglio di calcolo locale in PDF utilizzando l'API Aspose.Cells Cloud"
linktitle: "Converti foglio di calcolo in PDF"
type: docs
url: /convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, foglio di calcolo in PDF, conversione Excel, API cloud, generazione PDF, API REST, v4.0"
description: "Guida passo-passo per convertire un foglio di calcolo locale in PDF utilizzando l'API Aspose.Cells Cloud. Include sintassi della richiesta, parametri, dettagli della risposta, gestione degli errori e casi d'uso pratici."
weight: 100
---

L'endpoint **ConvertSpreadsheetToPdf** legge un file di foglio di calcolo caricato da un'unità locale, lo elabora sul server Aspose.Cells Cloud e restituisce il documento PDF risultante come flusso binario. Questa conversione nativa cloud elimina la necessità di caricare il file sorgente nello storage, riduce il consumo di risorse e semplifica i flussi di lavoro consegnando direttamente il PDF al client. I formati supportati dipendono dalle librerie sottostanti; l'API convalida l'esistenza del file, i permessi e l'integrità della conversione, generando opportuni errori HTTP in caso di input non validi o errori durante l'elaborazione.

## **API Converti foglio di calcolo in PDF**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome Parametro | Tipo   | Posizione | Obbligatorio/Opzionale | Descrizione                                                                                                                                                                                    |
| :------------- | :----- | :-------- | :--------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData  | Obbligatorio           | Il file del foglio di calcolo sorgente (XLS, XLSX, CSV, ecc.) da convertire. Deve essere un file valido e leggibile; la dimensione massima è di 100 MB. Esempio: `myWorkbook.xlsx`.        |
| outPath        | String | Query     | Opzionale              | Percorso della cartella di destinazione in cui salvare il PDF convertito sul server (se si desidera salvarlo). Se omesso, il file viene restituito direttamente nella risposta. Esempio: `/output/reports/`. |
| outStorageName | String | Query     | Opzionale              | Nome del servizio di storage di destinazione (es. `MyCloudStorage`). Obbligatorio solo se `outPath` è utilizzato e lo storage non è quello predefinito.                                          |
| fontsLocation  | String | Query     | Opzionale              | Percorso di una cartella personalizzata per i font sul server, per garantire una corretta resa del testo nel PDF. Esempio: `/fonts/custom/`.                                                     |
| region         | String | Query     | Opzionale              | Impostazione di regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione.       |
| password       | String | Query     | Opzionale              | Password necessaria per aprire un foglio di calcolo protetto. Omettere se il file non è crittografato.                                                                                          |

### **Risposta**

Risposta riuscita (200 OK)  
Content-Type: application/pdf  
Content‑Disposition: attachment; filename="converted.pdf"  
Content‑Length: `<dimensione in byte>`

Corpo: flusso binario del file PDF generato

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto sul server.                                     |

## Dove utilizzare l'API Converti foglio di calcolo in PDF?

- **Pipeline di generazione report automatizzate** – Converti report Excel generati quotidianamente in PDF per l'archiviazione o la distribuzione via email, senza interventi manuali.
- **Sistemi di gestione documenti** – Memorizza direttamente i PDF in un DMS dopo la conversione, conservando il foglio di calcolo originale solo sul lato client.
- **Applicazioni web con esportazione in tempo reale** – Consenti agli utenti finali di scaricare una versione PDF del foglio di calcolo che stanno modificando nel browser, sfruttando la conversione cloud per preservare il layout.
- **Conformità normativa** – Genera snapshot PDF immutabili di fogli di calcolo finanziari per tracciabilità durante gli audit, garantendo che il file sorgente non lasci mai l'ambiente client.
- **Flussi di lavoro di conversione multi-formato** – Combina con altri endpoint di conversione, come l'[API Converti foglio di calcolo in CSV](/convert-spreadsheet-to-csv/), per creare archivi multi-formato.

## Perché utilizzare l'API Converti foglio di calcolo in PDF?

- **Flusso di lavoro senza caricamento iniziale** – Nessuna necessità di caricare il file sorgente nello storage cloud; la conversione avviene direttamente dal flusso caricato, risparmiando larghezza di banda e costi di storage.
- **Rendering ad alta fedeltà** – Aspose.Cells preserva formule complesse, grafici e formattazioni durante la conversione in PDF, ottenendo risultati identici a quelli di Excel su desktop.
- **Esecuzione scalabile su cloud** – Sfrutta l'infrastruttura cloud di Aspose per conversioni rapide e affidabili, indipendentemente dall'hardware del client.
- **Interfaccia REST semplice** – Una singola richiesta `PUT` con parametri opzionali in query; restituisce un flusso PDF pronto al download, facilitando l'integrazione in qualsiasi linguaggio.

## Come utilizzare l'API Converti foglio di calcolo in PDF con gli SDK

### Specifica dell'API Converti foglio di calcolo in PDF

La [Specifica dell'API Converti foglio di calcolo in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) fornisce un'interfaccia di programmazione pubblicamente accessibile per eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. Il seguente esempio mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, permettendo di unire un foglio di calcolo in un altro con poche righe di codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud. I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells Cloud utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}