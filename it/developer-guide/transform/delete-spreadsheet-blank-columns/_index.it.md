---
title: Aspose.Cells Cloud Web API - Elimina colonne vuote nel foglio di calcolo
second_title: Documen
ArticleTitle: Delete Blank Columns in a Spreadshee
linktitle: Elimina colonna vuota
type: docs
url: /it/delete-spreadsheet-blank-columns/
keywords: Aspose.Cells Cloud Web API, Delete Blank Columns, Spreadsheet Cleanup, REST, Excel, Office Clou
description: Elimina in modo efficiente tutte le colonne vuote da un foglio di calcolo Excel, migliorando la gestione dei dati e l'usabilità
weight: 100
kwords: Excel, Office Cloud, Foglio di calcolo, PDF, CSV, JSON, Markdown, Rimuovi colonne vuote, Excel Pulizia foglio di lavoro
---
Eliminare tutte le colonne vuote che non contengono dati o altri oggetti da un foglio di calcolo Excel.

## **EliminaFoglio di calcoloColonne vuote AP**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo.|
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

## Dove dovremmo usare l'opzione Elimina colonne vuote del foglio di calcolo API?

Quando è necessario trasformare i dati, è possibile utilizzare questo API.

## Perché dovresti usare Elimina colonne vuote del foglio di calcolo API?

- Elimina rapidamente tutte le colonne vuote che non contengono dati o altri oggetti da un foglio di calcolo Excel.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare l'opzione Elimina colonne vuote del foglio di calcolo API con gli SDK

### Elimina le colonne vuote del foglio di calcolo API Specifiche

 IL[Elimina le colonne vuote del foglio di calcolo API Specifiche](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankColumns) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di eliminare le colonne vuote del foglio di calcolo con un codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{< /tab >}}
{{< /tabs >}}
