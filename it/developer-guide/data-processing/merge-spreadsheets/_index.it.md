---
title: Aspose.Cells Cloud Web API - Unisci più fogli di calcolo in un unico foglio di calcolo
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: Unisci foglio di calcolo
type: docs
url: /it/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: Unisci facilmente i file di fogli di calcolo locali in vari formati (XLSX, CSV, PDF) utilizzando Excel API
weight: 100
kwords: Excel API, Unisci fogli di calcolo, Office Cloud, REST API, Unione fogli di calcolo, Formato CSV, JSON, Markdow
---
Unisci più file di fogli di calcolo locali in un unico file, supportando l'output in oltre 30 formati di file.

## **Unisci foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| Foglio di calcolo| File| FormData| Carica il file del foglio di calcolo.|
| outFormat| Corda| Domanda| Specificare il formato del file di output.|
| mergeInOneSheet| Booleano| Domanda| Indica se combinare tutti i dati in un unico foglio di lavoro.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Percorso della cartella di lavoro di output. Il valore predefinito è null.|
|outStorageName| Corda| Domanda| Specificare il nome di archiviazione del file di output.|
| fontPosizione| Corda| Domanda| Definisci i font personalizzati da utilizzare.|
| regione| Corda| Domanda| Imposta l'area del foglio di calcolo.|
| password| Corda| Domanda| Fornire la password per aprire il file del foglio di calcolo.|

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

## Dove dovremmo utilizzare il Merge Local Spreadsheet API?

Quando è necessario unire più file di dati, è possibile utilizzare questo API.

## Perché dovresti usare il Merge Local Spreadsheet API?

- Non è necessario alcuno spazio di archiviazione cloud, basta unire direttamente.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di calcolo Merge Local API con gli SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)fornisce un'interfaccia di programmazione accessibile al pubblico, consentendo agli utenti di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di unire più fogli di calcolo in un unico foglio di calcolo con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
