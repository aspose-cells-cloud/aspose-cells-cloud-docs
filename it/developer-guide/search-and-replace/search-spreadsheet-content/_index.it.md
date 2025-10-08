---
title: Aspose.Cells Cloud Web API - Cerca contenuto foglio di calcolo
second_title: Documen
ArticleTitle: Search Spreadsheet Conten
linktitle: Cerca contenuto foglio di calcolo
type: docs
url: /it/search-spreadsheet-content/
keywords: Excel, Office Cloud, REST API, Spreadsheet Search, PDF Export, CSV Handling, JSON Formatting, Markdown Integration, Match Empty Cells in Exce
description: Cerca in modo efficiente il testo nei file di fogli di calcolo locali utilizzando il nostro API
weight: 100
kwords: Excel, Office Cloud, REST API, Ricerca foglio di calcolo, PDF Esportazione, Gestione CSV, Formattazione JSON, Integrazione Markdown, Corrispondenza vuota Cells in Excel
---
Cerca testo nei file di fogli di calcolo locali utilizzando il nostro API.

## **Cerca contenuto foglio di calcolo API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/content
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo da cercare.|
|testo di ricerca|Corda|Domanda|Il testo da cercare all'interno del foglio di calcolo.|
|ignorando il caso|Booleano|Domanda|Specificare se ignorare le maiuscole/minuscole nella ricerca.|
|foglio di lavoro|Corda|Domanda|Specificare il foglio di lavoro in cui effettuare la ricerca.|
|area della cella|Corda|Domanda|Specificare l'area delle celle da cercare.|
|regione|Corda|Domanda|Impostazione della regione per il foglio di calcolo.|
|password|Corda|Domanda|La password richiesta per aprire il file del foglio di calcolo.|

### **Risposta**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
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

## Dove dovremmo utilizzare il contenuto di ricerca all'interno del foglio di calcolo API?

Quando hai bisogno di cercare contenuti all'interno del foglio di calcolo, puoi utilizzare questo API.

## Perché dovresti usare il contenuto di ricerca all'interno del foglio di calcolo API?

- Cerca senza sforzo i contenuti all'interno di un foglio di calcolo con questo API.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la ricerca di link non funzionanti nel foglio di calcolo API con SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice i contenuti di ricerca all'interno dei fogli di calcolo per le celle con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
