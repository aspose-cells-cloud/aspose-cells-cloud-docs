---
title: Aspose.Cells Cloud Web API - Dividi un foglio di calcolo in più file, uno per ogni foglio di lavoro
second_title: Documen
ArticleTitle: Split a spreadsheet into multiple files, one for each worksheet
linktitle: Dividi foglio di calcolo remoto in Clou
type: docs
url: /it/split-remote-spreadsheet/
keywords: spreadsheet splitting, cloud spreadsheet API, split Excel file, multi-format outpu
description: Dividi un foglio di calcolo archiviato nel cloud in più formati di output senza scaricarlo
weight: 100
kwords: Excel, Office Cloud, REST, Foglio di calcolo, PDF, CSV, JSON, Markdown, foglio di calcolo remoto diviso
---
Suddividi il foglio di calcolo archiviato nel cloud in file separati con 30 formati di file di output.

## **Dividi foglio di calcolo remoto API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| nome| Corda| Sentiero| Nome del file della cartella di lavoro da dividere.|
| cartella| Corda| Domanda| Percorso della cartella in cui è archiviata la cartella di lavoro.|
| da| Intero| Domanda| Inizia l'indice del foglio di lavoro.|
| A| Intero| Domanda| Indice finale del foglio di lavoro.|
| outFormat| Corda| Domanda| Il formato di output desiderato (ad esempio, "Xlsx", "Pdf", "Csv").|
| Nome di archiviazione| Corda| Domanda|(Facoltativo) Il nome dell'archivio se si utilizza un archivio cloud personalizzato. Se omesso, utilizzare l'archivio predefinito.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
|outStorageName| Corda| Domanda| Nome di archiviazione del file di output.|
| fontPosizione| Corda| Domanda| Utilizza font personalizzati.|
| regione| Corda| Domanda| Impostazione della regione del foglio di calcolo.|
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

## Dove dovremmo utilizzare il foglio di calcolo remoto Split API?

Quando è necessario unire più file di dati, è possibile utilizzare questo API.

## Perché dovresti usare Split Remote Spreadsheet API?

- I file di archiviazione cloud non devono essere scaricati e possono essere suddivisi direttamente nel cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di calcolo remoto diviso API con gli SDK

### Specifiche del foglio di calcolo remoto diviso API

 IL[Specifiche del foglio di calcolo remoto diviso API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) definisce un'interfaccia di programmazione accessibile al pubblico e consente interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di suddividere il foglio di calcolo archiviato nel cloud in file separati tramite codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{< /tab >}}
{{< /tabs >}}
