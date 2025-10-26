---
title: Aspose.Cells Cloud Web API - Converti un grafico di foglio di calcolo in un'immagine
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: Converti grafico in immagine
type: docs
url: /it/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: Converti un grafico da un file di foglio di calcolo locale/Excel in un file immagine con Aspose.Cells Cloud Web API
weight: 100
kwords: convertire un grafico Excel in immagine, png, svg, tiff, jpg, bmp, foglio di calcolo
---
Converti un grafico da un file di foglio di calcolo locale/Excel in un file in formato immagine. Supportato**FORMATI IMMAGINE:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Converti grafico in immagine API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo contenente il grafico.|
|foglio di lavoro|Corda|Domanda|Specificare il nome del foglio di lavoro, se applicabile.|
|graficoIndice|Intero|Domanda|Indice del grafico da convertire.|
|formato|Corda|Domanda|(Obbligatorio) Il tipo di immagine desiderato (ad esempio, svg, png, jpg).|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Percorso della cartella in cui è archiviata la cartella di lavoro; il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome dell'archiviazione per il file di output.|
|fontPosizione|Corda|Domanda|Se necessario, specificare font personalizzati.|
|regione|Corda|Domanda|Imposta l'area del foglio di calcolo.|
|password|Corda|Domanda|La password per aprire il file del foglio di calcolo.|

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

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovresti usare Converti grafico in immagine API?

- Esportare i grafici nel foglio di calcolo come immagini.

## Perché dovresti usare Converti grafico in immagine API?

- Non è necessario alcuno spazio di archiviazione nel cloud, riducendo così il carico sulle risorse cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la conversione del grafico in immagine API con gli SDK?

### Converti grafico in immagine API Specifiche

 IL[Converti grafico in immagine API Specifiche](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di convertire un grafico in un'immagine con un codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
