---
title: "Aspose.Cells Cloud Web API - Converti grafico Excel in immagine - Strumento online gratuito"
second_title: "Documento"
ArticleTitle: "Come convertire un grafico in un foglio di calcolo in immagine: Guida passo-passo"
linktitle: "Converti grafico in immagine"
type: docs
url: /convert-chart-to-image/
keywords: "converti grafico in immagine, Aspose.Cells, esportazione grafico Excel, PNG, SVG, JPEG, BMP, TIFF"
description: "Usa l’API Web Aspose.Cells Cloud per convertire un grafico Excel in immagini PNG, SVG, TIFF, JPEG o BMP direttamente da un file di foglio di calcolo."
weight: 100
---

I grafici Excel sono rappresentazioni visive dei dati che possono essere incorporati all'interno dei fogli di lavoro. Convertire questi grafici in formati immagine consente un facile riutilizzo in documenti, pagine web e report, senza richiedere l'installazione di Excel.

Converti un grafico da un foglio di calcolo locale o da un file Excel in un'immagine. **FORMATI IMMAGINE SUPPORTATI:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **Converti grafico in immagine tramite API**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo    | Percorso/Query string/HTTPBody | Descrizione                                                                        | Obbligatorio |
| :------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------- | :------- |
| Spreadsheet    | File    | FormData                   | Carica il file di foglio di calcolo contenente il grafico.                         | Sì       |
| worksheet      | String  | Query                      | Specifica il nome del foglio di lavoro, se applicabile.                            | No       |
| chartIndex     | Integer | Query                      | Indice del grafico da convertire.                                                  | Sì       |
| format         | String  | Query                      | (Obbligatorio) Tipo di immagine desiderato (es. svg, png, jpg).                    | Sì       |
| outPath        | String  | Query                      | (Opzionale) Percorso della cartella in cui verrà salvato il file in output; default: null. | No       |
| outStorageName | String  | Query                      | Nome dello storage in cui salvare il file in output.                               | No       |
| fontsLocation  | String  | Query                      | Specifica i caratteri personalizzati, se necessari.                                | No       |
| region         | String  | Query                      | Imposta la regione del foglio di calcolo.                                          | No       |
| password       | String  | Query                      | Password per aprire il file di foglio di calcolo.                                  | No       |

## **Risposta**

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
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida  | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401  | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413  | Payload troppo grande | Il file caricato supera il limite di dimensione.                  |
| 500  | Errore interno del server | Errore imprevisto del server.                                     |

## Dove dovresti usare l’API Converti grafico in immagine?

- **Generazione di report e dashboard**: converti automaticamente i grafici dai dati Excel in immagini (PNG, JPEG, ecc.) da incorporare in report PDF, dashboard web o presentazioni PowerPoint.
- **Applicazioni web/e-mail**: restituisci immagini dei grafici direttamente nelle pagine web o nelle e-mail, senza richiedere agli utenti di scaricare o aprire file Excel. Utile per strumenti di reportistica dinamica, newsletter o notifiche automatizzate.
- **Flussi di lavoro di elaborazione documenti**: integra in pipeline automatizzate (es. fatturazione, analisi) in cui i grafici Excel devono essere inseriti in altri formati (Word, PDF, HTML).
- **Applicazioni mobile/desktop**: visualizza i grafici Excel in app dove il rendering completo del foglio di calcolo non è necessario o pratico.
- **Archiviazione e visualizzazione**: salva i grafici come immagini autonome per archiviazione a lungo termine, anteprime o miniature, senza dipendenze da Excel.

## Perché dovresti usare l’API Converti grafico in immagine?

- **Preserva la fedeltà visiva**: mantiene la formattazione esatta del grafico (colori, etichette, scala) come visibile in Excel, garantendo un output di qualità professionale.
- **Indipendente dalla piattaforma**: non richiede l'installazione di Excel. Funziona su diverse piattaforme (Windows, Linux, macOS) tramite API REST, adatto per applicazioni cloud o lato server.
- **Automazione e scalabilità**: converti in batch più grafici o file programmaticamente, risparmiando tempo rispetto all'esportazione manuale. Gestisce grandi volumi in modo efficiente nel cloud.
- **Formati di output flessibili**: supporta formati immagine popolari (PNG, JPG, BMP, SVG, ecc.), consentendo l'integrazione con sistemi e supporti diversi.
- **Sicuro e affidabile**: elabora i file nell'ambiente cloud di Aspose senza esporre dati sensibili a strumenti lato client. Alta disponibilità e prestazioni costanti.
- **Facile per gli sviluppatori**: Aspose.Cells Cloud offre SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da documentazione completa. Rispetto alla creazione di soluzioni personalizzate di rendering grafico, riduce significativamente lo sforzo di sviluppo.
- **Conveniente**: puoi convertire grafici senza caricare preventivamente il workbook, risparmiando spazio di archiviazione e riducendo i costi.

## Come usare l’API Converti grafico in immagine con gli SDK?

### Specifica dell’API Converti grafico in immagine

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">Specifica dell’API Converti grafico in immagine</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

### Usa gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il metodo più rapido per sviluppare, poiché nasconde i dettagli di basso livello, consentendo di convertire un grafico in immagine con poche righe di codice.  
Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells usando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}