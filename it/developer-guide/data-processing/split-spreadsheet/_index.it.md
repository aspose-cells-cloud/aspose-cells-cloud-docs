---
title: Aspose.Cells Cloud WEb API - Dividi il foglio di calcolo in file separati
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: Foglio di calcolo diviso
type: docs
url: /it/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: Dividi un foglio di calcolo locale in più file in vari formati senza richiedere l'archiviazione nel cloud
weight: 100
kwords: Excel API, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Foglio di calcolo locale diviso, Elaborazione cloud, Gestione file, Gestione errori
---
Suddividi il foglio di calcolo locale in file separati con 30 formati di file di output senza richiedere l'archiviazione nel cloud.

## **Foglio di calcolo diviso API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| Foglio di calcolo| File| FormData| Carica il file del foglio di calcolo da dividere.|
| da| Intero| Domanda| Specificare l'indice iniziale del foglio di lavoro.|
| A| Intero| Domanda| Specificare l'indice finale del foglio di lavoro.|
| outFormat| Corda| Domanda| Definire il formato del file di output.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Percorso della cartella in cui archiviare la cartella di lavoro di output. Il valore predefinito è null.|
|outStorageName| Corda| Domanda| Definire il nome di archiviazione del file di output.|
| fontPosizione| Corda| Domanda| Se necessario, specificare font personalizzati.|
| ricominciare| Corda| Domanda| Imposta l'area del foglio di calcolo.|
| password| Corda| Domanda| Fornire la password per accedere al file del foglio di calcolo.|

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

## Dove dovremmo usare il foglio di calcolo diviso API?

Quando hai bisogno di dividere un foglio di calcolo in più file, puoi usare questo API.

## Perché dovresti usare Split Spreadsheet API?

- Non c'è bisogno di spazio di archiviazione cloud, basta dividerlo direttamente.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di calcolo diviso API con gli SDK

### Specifiche del foglio di calcolo diviso API

 IL[Specifiche del foglio di calcolo diviso API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) fornisce un'interfaccia di programmazione accessibile al pubblico per eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di suddividere il foglio di calcolo in file separati con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come richiamare i servizi Web Aspose.Cells utilizzando diversi SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
