---
title: Aspose.Cells Cloud Web API - Salva il foglio di calcolo come file di formato
second_title: Documen
ArticleTitle: Save Spreadsheet as a Format fil
linktitle: Salva foglio di calcolo a
type: docs
url: /it/save-spreadsheet-as/
keywords: spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, RES
description: Converti senza sforzo i fogli di calcolo archiviati nel cloud in vari formati, tra cui XLSX, PDF e CSV, utilizzando il nostro robusto API
weight: 100
kwords: Excel API, Office Cloud, REST, Foglio di calcolo, PDF, CSV, JSON, Markdown, converti Excel file, salva foglio di calcolo come, Aspose.Cells Cloud Web AP
---
Salva un file cloud spreadsheet/Excel come file di formato nell'archivio cloud.

## **Salva foglio di calcolo come API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| nome| Corda| Sentiero| (Obbligatorio) Il nome del file della cartella di lavoro da convertire.|
| formato| Corda| Domanda| (Obbligatorio) Il formato di output desiderato (ad esempio, "Xlsx", "Pdf", "Csv").|
| salvaOpzioniDati| Classe| Corpo| (Facoltativo) Salva i dati delle opzioni. Il valore predefinito è null.|
| cartella| Corda| Domanda| (Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
| Nome di archiviazione| Corda| Domanda|(Facoltativo) Il nome dell'archivio se si utilizza un archivio cloud personalizzato. Se omesso, utilizzare l'archivio predefinito.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
|outStorageName| Corda| Domanda| Nome di archiviazione del file di output.|
| fontPosizione| Corda| Domanda| Utilizza caratteri personalizzati.|
| regione| Corda| Domanda| Impostazione della regione del foglio di calcolo.|
| password| Corda| Domanda| La password per aprire il file del foglio di calcolo.|

### **Risposta**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Perché dovresti usare Save Spread API?

- Puoi convertire i file cloud in diversi formati sempre e ovunque.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la conversione da tabella a JSON API con gli SDK?

### Salva foglio di calcolo come API Specifiche

 IL[Salva foglio di calcolo come API Specifiche](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) definisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di salvare un foglio di calcolo come file di formato con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{< /tab >}}
{{< /tabs >}}
