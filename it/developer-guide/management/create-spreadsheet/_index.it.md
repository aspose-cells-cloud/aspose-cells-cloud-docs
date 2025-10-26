---
title: Aspose.Cells Cloud Web API - Crea un nuovo foglio di calcolo con un modello di foglio di calcolo
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: Crea foglio di calcolo
type: docs
url: /it/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: Excel API consente agli utenti di creare un nuovo foglio di calcolo con un nome specificato, supportando modelli opzionali per contenuti o formattazioni predefiniti, migliorando la produttività dell'utente
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel, Creazione di fogli di calcolo, Supporto modelli, Miglioramento della produttività
---
Crea un nuovo foglio di calcolo, che può essere vuoto o utilizzabile, creato in base al modello specificato.

## **Crea foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|---------- ||----------------------- |----- |
|formato| Corda| Domanda| Specifica il nome del nuovo foglio di calcolo. Questo nome verrà utilizzato per identificare il foglio di calcolo nel sistema.|
| modello| Corda| Domanda| Facoltativo. Se specificato, il nuovo foglio di calcolo verrà creato in base al modello specificato. Questo può essere utile per applicare layout e stili predefiniti.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
| outStorageName| Corda| Domanda| Nome di archiviazione del file di output.|
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

## Dove dovremmo usare Create Spreadsheet API?

Quando hai bisogno di creare un nuovo foglio di calcolo, puoi usare questo API.

## Perché dovresti usare Create Spreadsheet API?

- Non solo puoi creare un foglio di calcolo vuoto, ma puoi anche creare un foglio di calcolo specifico basato su un modello.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di calcolo API con gli SDK

### Crea foglio di calcolo API Specifiche

 IL[Crea foglio di calcolo API Specifiche](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) definisce un'interfaccia di programmazione accessibile al pubblico e consente interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di creare il foglio di calcolo con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
