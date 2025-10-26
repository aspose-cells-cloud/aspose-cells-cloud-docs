---
title: Aspose.Cells Cloud Web API - Conversione di un grafico di un foglio di calcolo in un file PDF
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: Converti grafico in PD
type: docs
url: /it/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: Questo API converte i grafici dai fogli di calcolo situati su un'unità locale al file PDF senza problemi
weight: 100
kwords: Excel, Office Cloud, REST API, Conversione foglio di calcolo, PDF, CSV, JSON, Markdown, Converti grafico in PDF, Conversione cloud
---
 Convertire un grafico da un file di foglio di calcolo locale/Excel a un[PDF](https://docs.fileformat.com/pdf/) file.

## **Converti grafico in PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|-------------- ||--------------------- |--------------------------------------------------- |
| Foglio di calcolo|File| FormData| Carica il file del foglio di calcolo.|
| foglio di lavoro| Corda| Domanda| Il nome del foglio di lavoro contenente il grafico.|
| graficoIndice|Intero| Domanda| L'indice del grafico da convertire.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Il percorso della cartella in cui è archiviato il file convertito. Il valore predefinito è null.|
| outStorageName| Corda| Domanda| Nome di archiviazione del file di output.|
| fontPosizione| Corda| Domanda| Se necessario, utilizzare font personalizzati.|
| regione| Corda| Domanda| Impostazione della regione del foglio di calcolo.|
| password| Corda| Domanda| La password per aprire il file del foglio di calcolo.|

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

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovresti usare il Converti grafico in PDF API?

- Esportare i grafici nel foglio di calcolo in formato PDF.

## Perché dovresti usare il Converti grafico in PDF API?

- Non è necessario alcuno spazio di archiviazione nel cloud, riducendo così il carico sulle risorse cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il Converti grafico in PDF API con gli SDK?

### Converti grafico in PDF API Specifiche

 IL[Converti grafico in PDF API Specifiche](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

## Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di convertire un grafico in un file PDF con codice breve.
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
