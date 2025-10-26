---
title: Aspose.Cells Cloud Web API - Converti i dati di un intervallo di foglio di calcolo in un file CSV
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to a CSV file.
linktitle: Converti intervallo in CS
type: docs
url: /it/convert-range-to-csv/
keywords: Convert range to csv, convert spreadsheet to csv, Aspose Cloud Web API, cloud conversion, Excel to cs
description: Converti un intervallo specificato da un file di foglio di calcolo locale in un formato CSV utilizzando Excel API, garantendo un'esecuzione cloud senza interruzioni
weight: 100
kwords: intervallo in csv, convertire foglio di calcolo in csv, Aspose Cloud Web API, conversione cloud, Excel in csv
---
 Convertire un intervallo di dati da un file di foglio di calcolo locale/Excel a un[CSV](https://docs.fileformat.com/spreadsheet/csv/) file.

## **Converti intervallo in CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo.|
|foglio di lavoro|Corda|Domanda|Il nome del foglio di lavoro Spreadsheet/Excel|
|allineare|Corda|Domanda|Specificare l'area della cella (ad esempio, A1:C10).|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Percorso della cartella in cui verrà archiviata la cartella di lavoro. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome dell'archivio del file di output.|
|fontPosizione|Corda|Domanda|Se necessario, specificare font personalizzati.|
|regione|Corda|Domanda|Definisce l'impostazione della regione del foglio di calcolo.|
|password|Corda|Domanda|Password richiesta per aprire il file del foglio di calcolo.|

### **Risposta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream",
        }
    }
]
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Perché dovresti usare Converti grafico in CSV API?

- Non è necessario alcuno spazio di archiviazione nel cloud, riducendo così il carico sulle risorse cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il convertitore grafico in CSV API con gli SDK?

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) descrive un API accessibile al pubblico, che consente interazioni REST direttamente da un browser web.

## Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di convertire un intervallo di dati in un file CSV con codice breve.
 Esplora l'elenco completo degli SDK Cloud Aspose.Cells nel nostro[Repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice illustrano come chiamare i servizi Web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
