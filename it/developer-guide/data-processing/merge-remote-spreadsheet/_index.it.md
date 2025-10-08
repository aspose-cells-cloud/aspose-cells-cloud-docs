---
title: Aspose.Cells Cloud Web API - Unisci un foglio di calcolo in un altro.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: Unisci foglio di calcolo remoto
type: docs
url: /it/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: Combina un file di foglio di calcolo archiviato in un archivio cloud con un altro foglio di calcolo e potrai specificare il formato e la posizione dei dati in output.
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, unisci celle vuote, elaborazione cloud
---
Combina un file di foglio di calcolo archiviato in un archivio cloud con un altro foglio di calcolo e potrai specificare il formato e la posizione dei dati in output.

## **Unisci foglio di calcolo remoto API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|nome|Corda|Sentiero|Nome del file della cartella di lavoro da unire.|
|foglio di calcolo unito|Corda|Domanda|L'elenco dei file di foglio di calcolo da unire.|
|cartella|Corda|Domanda|Percorso della cartella in cui è archiviata la cartella di lavoro.|
|outFormat|Corda|Domanda|Formato del file di output (ad esempio, XLSX, PDF).|
|mergeInOneSheet|Booleano|Domanda|Se combinare tutti i dati in un unico foglio di lavoro.|
|Nome di archiviazione|Corda|Domanda|(Facoltativo) Il nome dell'archiviazione se si utilizza un archivio cloud personalizzato. Se omesso, il valore predefinito è l'archiviazione predefinita.|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Percorso della cartella di lavoro unita. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome dell'archivio per il file di output.|
|fontPosizione|Corda|Domanda|Posizione personalizzata del font.|
|regione|Corda|Domanda|Impostazione della regione del foglio di calcolo.|
|password|Corda|Domanda|La password per accedere al file del foglio di calcolo.|

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

## Dove dovremmo utilizzare il Merge Remote Spreadsheet API?

- Quando è necessario unire più file di dati insieme nell'archiviazione cloud.


## Perché dovresti usare Merge Remote Spreadsheet API?

- I file di archiviazione cloud non devono essere scaricati e possono essere uniti direttamente nel cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di calcolo remoto Merge API con gli SDK

### Specifiche di Merge Remote Spreadsheet API

 IL[Specifiche di Merge Remote Spreadsheet API](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) fornisce un'interfaccia di programmazione accessibile al pubblico per eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di unire un foglio di calcolo a un altro foglio di calcolo con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
I seguenti esempi di codice mostrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
