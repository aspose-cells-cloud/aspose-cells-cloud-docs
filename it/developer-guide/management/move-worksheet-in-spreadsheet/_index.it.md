---
title: Aspose.Cells Cloud Web API - Sposta un foglio di lavoro in una nuova posizione nel foglio di calcolo
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: Sposta il foglio di lavoro nel foglio di calcolo
type: docs
url: /it/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: MoveWorksheet API consente agli utenti di riposizionare in modo efficiente un foglio di lavoro specificato all'interno di una cartella di lavoro, migliorando così l'organizzazione e l'accessibilità dei dati del foglio di calcolo
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, Sposta foglio di lavoro, Organizzazione cartella di lavoro, PDF, CSV, JSON, Markdown
---
Sposta un foglio di lavoro in una nuova posizione in un foglio di calcolo.

## **Sposta il foglio di lavoro dal foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo.|
|foglio di lavoro|Corda|Domanda|Nome corrente del foglio di lavoro da spostare.|
|posizione|Intero|Domanda|La nuova posizione del foglio di lavoro.|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome di archiviazione del file di output.|
|regione|Corda|Domanda|Impostazione della regione del foglio di calcolo.|
|password|Corda|Domanda|La password per aprire il file del foglio di calcolo.|

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

## Dove dovremmo usare il foglio di lavoro Sposta nel foglio di calcolo API?

Quando è necessario spostare un foglio di lavoro in una nuova posizione nei fogli di calcolo, è possibile utilizzare questo API.

## Perché dovresti usare il foglio di lavoro Sposta nel foglio di calcolo API?

- Sposta rapidamente i fogli di lavoro dai fogli di calcolo.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di lavoro Sposta in Foglio di calcolo API con SDK

### Sposta foglio di lavoro in foglio di calcolo API Specifiche

 IL[Sposta foglio di lavoro in foglio di calcolo API Specifiche](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) fornisce un'interfaccia di programmazione accessibile al pubblico per facilitare le interazioni REST dirette da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di spostare il foglio di lavoro nel foglio di calcolo con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
I seguenti esempi di codice mostrano come chiamare i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
