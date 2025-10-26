---
title: Aspose.Cells Cloud Web API - Unisci i file di foglio di calcolo corrispondenti in un file in una cartella remota
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: Unisci fogli di calcolo in cartelle remote
type: docs
url: /it/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: Combina i file del foglio di calcolo archiviati nell'archiviazione cloud in un unico file e il formato del file supporta 30 formati per l'output, come PDF, Csv, Json e altri formati comuni
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Unisci fogli di calcolo, Elaborazione cloud, Gestione file remota
---
Unisci i file di fogli di calcolo corrispondenti nei file nella cartella remota; il formato del file di output supporta oltre 30 formati, come PDF, Csv, Json e altri formati comuni.


## **Unisci fogli di calcolo nella cartella remota API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| cartella| Corda| Domanda|La cartella in cui verranno archiviati i file uniti.|
| fileMatchExpression| Corda| Domanda| Espressione per abbinare i file da unire.|
| outFormat| Corda| Domanda| Formato del file di output desiderato.|
| mergeInOneSheet| Booleano| Domanda| Indica se combinare tutti i dati in un unico foglio di lavoro.|
| Nome di archiviazione| Corda| Domanda| (Facoltativo) Nome dell'archiviazione cloud personalizzata; se omessa, per impostazione predefinita viene utilizzata l'archiviazione predefinita.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Percorso della cartella in cui archiviare la cartella di lavoro; il valore predefinito è null.|
|outStorageName| Corda| Domanda| Nome dell'archivio per il file di output.|
| fontPosizione| Corda| Domanda| Specifica i font personalizzati.|
| regione| Corda| Domanda| Imposta l'area del foglio di calcolo.|
| password| Corda| Domanda| La password per aprire il file del foglio di calcolo.|

## **Risposta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovremmo utilizzare il foglio di calcolo Merge nella cartella remota API?

Quando è necessario unire più file di dati, è possibile utilizzare questo API.

## Perché dovresti usare il foglio di calcolo Merge nella cartella remota API?

- I file di archiviazione cloud non devono essere scaricati e possono essere uniti direttamente nel cloud.
- Unisci in batch più file di fogli di calcolo, supporta l'espressione corrispondente.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di calcolo Merge nella cartella remota API con gli SDK

### Unisci foglio di calcolo nella cartella remota API Specifiche

 IL[Unisci foglio di calcolo nella cartella remota API Specifiche](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) fornisce un'interfaccia di programmazione accessibile al pubblico che consente interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di unire i file di foglio di calcolo corrispondenti nei file nella cartella remota tramite codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
