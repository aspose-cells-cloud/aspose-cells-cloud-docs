---
title: Aspose.Cells Cloud Web API - Esporta un grafico di foglio di calcolo come file di formato
second_title: Documen
ArticleTitle: Export a Spreadsheet Chart as a Format fil
linktitle: Esporta grafico come formato
type: docs
url: /it/export-chart-as-format/
keywords: Export Chart, Aspose.Cells Cloud Web API, Spreadsheet Conversion, PDF Export, Image Export, REST, Excel, CSV, JSO
description: Converte in modo efficiente i grafici dai fogli di calcolo archiviati nel cloud in formati specifici come PDF o immagine direttamente senza scaricarli
weight: 100
kwords: Esporta grafico, REST, conversione foglio di calcolo, PDF, CSV, JSON, Markdown, Excel, formato immagine
---
Esporta un grafico/foglio di calcolo cloud Excel in un altro file di formato con Aspose.Cells Cloud Web API.

## **Esporta grafico come formato API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| nome| Corda| Sentiero| (Obbligatorio) Il nome del file della cartella di lavoro da recuperare.|
| foglio di lavoro| Corda| Sentiero| Nome del foglio di lavoro|
| graficoIndice| Intero| Sentiero| Indice del grafico|
| formato| Corda| Domanda| (Obbligatorio) Il formato di output desiderato (ad esempio, "png", "pdf", "svg").|
| cartella| Corda| Domanda| (Facoltativo) Percorso della cartella in cui è archiviata la cartella di lavoro; il valore predefinito è null.|
| Nome di archiviazione| Corda| Domanda|(Facoltativo) Il nome dell'archiviazione se si utilizza un archivio cloud personalizzato; se omesso, utilizzare l'archiviazione predefinita.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Percorso della cartella in cui è archiviata la cartella di lavoro; il valore predefinito è null.|
|outStorageName| Corda| Domanda| Nome di archiviazione del file di output.|
| fontPosizione| Corda| Domanda| Utilizza font personalizzati.|
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

## Perché dovresti usare il grafico del foglio di calcolo di esportazione nel formato API?

- Puoi convertire i file cloud in diversi formati sempre e ovunque.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il grafico del foglio di calcolo di esportazione nel formato API con gli SDK?

### Esporta grafico come formato API Specifiche

 IL[Esporta grafico come formato API Specifiche](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat) definisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di esportare i dati di un grafico di foglio di calcolo in un file di formato con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
