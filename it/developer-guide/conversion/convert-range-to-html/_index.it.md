---
title: Aspose.Cells Cloud Web API - Conversione dell'intervallo del foglio di calcolo in HTM
second_title: Documen
ArticleTitle: Converting Spreadsheet Range to Htm
linktitle: Converti intervallo in HTM
type: docs
url: /it/convert-range-to-html/
keywords: Convert a spreadsheet range data to a html file, Spreadsheet Conversion, Excel Conversio
description: Converti un intervallo da un file di foglio di calcolo locale/Excel in un file HTML con Aspose.Cells Cloud Web API
weight: 100
kwords: Converti intervallo in HTML, Foglio di calcolo, Excel
---
Convertire un intervallo di dati da un file spreadsheet/Excel locale in un file HTML.

## **Converti intervallo in HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/html
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|------------|--|------------------------|-------------------------------------------------|
| Foglio di calcolo|File| FormData| Carica il file del foglio di calcolo.|
| foglio di lavoro| Corda| Domanda| Nome del foglio di lavoro all'interno del foglio di calcolo.|
| allineare| Corda| Domanda| L'area della cella da convertire, ad esempio A1:C10.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
| outStorageName| Corda| Domanda| Nome dell'archivio del file di output.|
| fontPosizione| Corda| Domanda| Specificare i font personalizzati da utilizzare.|
| regione| Corda| Domanda| Impostazione della regione del foglio di calcolo.|
| password| Corda| Domanda| Password per aprire il file del foglio di calcolo.|

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

## Perché dovresti usare Converti intervallo in HTML API?

- Non è necessario alcuno spazio di archiviazione nel cloud, riducendo così il carico sulle risorse cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare l'intervallo di conversione in HTML API con gli SDK?

### Converti intervallo in HTML API Specifiche

 IL[Converti intervallo in HTML API Specifiche](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) fornisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di convertire un intervallo di dati in un file HTML con codice breve.
 Si prega di visitare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
