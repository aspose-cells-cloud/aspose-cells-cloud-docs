---
title: Aspose.Cells Cloud Web API - Elimina le righe vuote nel foglio di calcolo
second_title: Documen
ArticleTitle: Delete Blank Rows in a Spreadshee
linktitle: Elimina riga vuota
type: docs
url: /it/delete-spreadsheet-blank-rows/
keywords: Delete blank rows, Excel API, Spreadsheet cleaning, Aspose.Cells Cloud Web API, Remove empty row
description: Elimina in modo efficiente tutte le righe vuote in un foglio di calcolo che non contengono dati o oggetti, migliorando l'organizzazione dei dati
weight: 100
kwords: Excel, REST, Foglio di calcolo, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel, Rimuovi righe vuote
---
Eliminare tutte le righe vuote che non contengono dati o altri oggetti da un foglio di calcolo Excel.

## **EliminaFoglio di calcoloRighe vuote AP**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo.|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome dell'archivio del file di output.|
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

## Dove dovremmo usare Elimina righe vuote del foglio di calcolo API?

Quando è necessario trasformare i dati, è possibile utilizzare questo API.

## Perché dovresti usare Elimina righe vuote del foglio di calcolo API?

- Elimina rapidamente tutte le righe vuote che non contengono dati o altri oggetti da un foglio di calcolo Excel.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare l'opzione Elimina righe vuote del foglio di calcolo API con gli SDK

### Elimina le righe vuote del foglio di calcolo API Specifiche

 IL[Elimina le righe vuote del foglio di calcolo API Specifiche](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di eliminare le righe vuote del foglio di calcolo con un codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}
{{< /tab >}}
{{< /tabs >}}
