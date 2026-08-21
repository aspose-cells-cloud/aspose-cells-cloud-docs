---
title: "Conversione di foglio di lavoro – Documentazione dell'API Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Come convertire i dati di un foglio di calcolo locale in un file immagine: Guida passo-passo"
linktitle: "Converti foglio di lavoro in immagine"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, conversione foglio di lavoro in immagine, converti foglio di lavoro in immagine, Excel in PNG, Excel in SVG, Excel in TIFF, Excel in JPEG, Excel in BMP, API per la conversione immagine, API REST, esportazione immagine foglio di calcolo, esempi SDK"
description: "Guida passo-passo per convertire un foglio di calcolo Excel in formati immagine (PNG, SVG, TIFF, JPEG, BMP, ecc.) utilizzando l'API Aspose.Cells Cloud, inclusi parametri di richiesta, dettagli della risposta, codici di errore, scenari di utilizzo ed esempi di codice SDK."
weight: 100
---

Esporta i dati di un foglio di lavoro da un file Excel locale in un file [Immagine](https://docs.fileformat.com/image/) utilizzando l'API Aspose.Cells Cloud. Questa operazione supporta diversi formati immagine ed è ideale per generare istantanee visive dei dati del foglio di calcolo.

**FORMATI IMMAGINE SUPPORTATI**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API Converti foglio di lavoro in immagine**

### API Web

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo   | Percorso/Query string/HTTPBody | Descrizione                                                                                  |
| :------------- | :----- | :----------------------------- | :------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                       | Carica il file del foglio di calcolo.                                                        |
| worksheet      | String | Query                          | Nome del foglio di lavoro da convertire.                                                     |
| format         | String | Query                          | Formato immagine desiderato (`svg`, `png`, `tiff`, `jpeg`, `bmp`, ecc.).                     |
| outPath        | String | Query                          | _(Opzionale)_ Percorso della cartella in cui verrà salvata l'immagine di output; valore predefinito `null`. |
| outStorageName | String | Query                          | Nome della posizione di archiviazione per il file di output.                                 |
| fontsLocation  | String | Query                          | Percorso di una cartella di caratteri personalizzati, se è necessario utilizzare caratteri non disponibili sul server. |
| region         | String | Query                          | Impostazione della regione del foglio di calcolo (ad esempio, `en-US`).                      |
| password       | String | Query                          | Password necessaria per aprire un file di foglio di calcolo protetto.                        |

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

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno server | Errore imprevisto del server.                                     |

## **Dove dovresti utilizzare l'API Converti foglio di lavoro in immagine?**

- **Istantanee di report statici** – Converti tabelle finanziarie, calcoli o altri dati in immagini da includere in report PDF, diapositive PowerPoint o documenti stampati, quando non è richiesta la modifica.
- **Visualizzazione dei dati nelle presentazioni** – Trasforma tabelle complesse del foglio di calcolo (inclusi formattazioni condizionali o grafici semplici) in immagini da incorporare nelle presentazioni (PPTX, Google Slides).
- **Documentazione e materiali formativi** – Cattura esempi di fogli di calcolo, modelli o moduli di immissione dati come immagini per manuali utente, tutorial o articoli della knowledge base.
- **Anteprime in miniatura** – Genera piccole anteprime immagine di sezioni chiave del foglio di calcolo per browser di file, librerie di documenti o risultati di ricerca.

## Perché dovresti utilizzare l'API Converti foglio di lavoro in immagine?

- **Facile per lo sviluppatore** – Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido, e dispone di una documentazione completa. Rispetto alla creazione di una soluzione personalizzata per il rendering dei grafici, riduce significativamente il carico di lavoro di sviluppo.
- **Conveniente** – Puoi convertire i dati delle tabelle senza dover conservare permanentemente il file del workbook, risparmiando spazio di archiviazione e riducendo i costi.
- **Preservazione perfetta dei pixel** – Riproduce fedelmente l'aspetto di Excel, inclusa la formattazione delle celle, le formule (come valori visualizzati), bordi, colori e formattazione condizionale, nell'immagine di output.
- **Compatibilità universale** – I formati immagine (PNG, JPEG, TIFF, BMP, SVG, ecc.) sono visualizzabili su qualsiasi dispositivo o piattaforma senza software specializzati, garantendo la massima accessibilità.

## Come utilizzare l'API Converti foglio di lavoro in immagine con gli SDK?

### Specifica dell'API Converti foglio di lavoro in immagine

La [Specifiche dell'API Converti foglio di lavoro in immagine](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) definisce un'interfaccia di programmazione pubblicamente accessibile e consente interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
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
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello e consente di convertire i dati del foglio di lavoro in immagine con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}