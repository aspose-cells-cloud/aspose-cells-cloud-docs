---
title: Aspose.Cells Cloud Web API - Importa dati CSV, JSON o XML in un file di foglio di calcolo
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: Importa dati in un foglio di calcolo
type: docs
url: /it/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: Importa in modo efficiente i dati in un foglio di calcolo da formati supportati come CSV, JSON e XML utilizzando Aspose.Cells Cloud Web API
weight: 100
kwords: Aspose.Cells Cloud Web API, Importa dati, Office Cloud, REST, Foglio di calcolo, CSV, JSON, XM
---
 Importa dati in un foglio di calcolo. Il formato supportato del file di dati importato è[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) O[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **Importa dati nel foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| file di dati| File| FormData| Carica il file di dati da importare.|
| Foglio di calcolo| File| FormData| Carica il file del foglio di calcolo di destinazione.|
| foglio di lavoro| Corda| Domanda| Specificare il foglio di lavoro per l'importazione dei dati.|
| cellula di partenza| Corda| Domanda|Specificare la posizione iniziale per l'importazione dei dati.|
| inserire| Booleano| Domanda| Indica se inserire o sovrascrivere i dati di importazione specificati.|
| convertNumericData| Booleano| Domanda| Specificare se convertire i dati numerici durante l'importazione.|
| divisore| Corda| Domanda| Specificare il delimitatore per il formato CSV.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
|outStorageName| Corda| Domanda| Specificare il nome di archiviazione del file di output.|
| fontPosizione| Corda| Domanda| Definisci i font personalizzati da utilizzare.|
| ricominciare| Corda| Domanda| Imposta la configurazione della regione del foglio di calcolo.|
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

## Dove dovremmo usare l'importazione dei dati nel foglio di calcolo API?

- Importazione di grandi quantità di dati in un foglio di calcolo.
-  Il formato del file di dati importato è[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) E[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## Perché dovresti usare l'importazione di dati in un foglio di calcolo API?

- Importazione di grandi quantità di dati in fogli di calcolo.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare l'importazione di dati in un foglio di calcolo API con gli SDK

### Importa dati in foglio di calcolo API Specifiche

 IL[Importa dati in foglio di calcolo API Specifiche](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) fornisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente dal tuo browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di importare i dati in un foglio di calcolo con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come richiamare i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
