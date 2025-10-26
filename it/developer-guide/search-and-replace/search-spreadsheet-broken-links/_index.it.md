---
title: Aspose.Cells Cloud Web API - Cerca i link non funzionanti in un foglio di calcolo
second_title: Documen
ArticleTitle: Search Spreadsheet Broken Links in a Spreadshee
linktitle: Cerca collegamento non funzionante nel foglio di calcolo
type: docs
url: /it/search-spreadsheet-broken-links/
keywords: search broken links, spreadsheet API, Excel broken links, REST API, Office Cloud integratio
description: Cerca in modo efficiente i link non funzionanti nei fogli di calcolo locali utilizzando Excel API
weight: 100
kwords: Excel API, ricerca link non funzionanti, Office Cloud, REST API, gestione fogli di calcolo, PDF, CSV, JSON, Markdown, identificazione link non funzionanti, riparazione collegamento ipertestuale
---
Cerca i link non funzionanti nei fogli di calcolo locali.

## **Cerca collegamenti interrotti nel foglio di calcolo API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/broken-links
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo da analizzare.|
|foglio di lavoro|Corda|Domanda|Specificare il foglio di lavoro per l'esame.|
|area della cella|Corda|Domanda|Definire l'area della cella da analizzare.|
|regione|Corda|Domanda|Imposta la configurazione della regione del foglio di calcolo.|
|password|Corda|Domanda|Fornire la password per accedere al file del foglio di calcolo.|

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

## Dove dovremmo usare la funzione Cerca link non funzionanti all'interno del foglio di calcolo API?

Quando hai bisogno di cercare link non funzionanti all'interno del foglio di calcolo, puoi usare questo API.

## Perché dovresti usare la funzione Cerca link non funzionanti nel foglio di calcolo API?

- Cerca senza sforzo i link non funzionanti all'interno di un foglio di calcolo remoto con questo API.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la ricerca di link non funzionanti nel foglio di calcolo API con SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks) definisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice i link interrotti di ricerca all'interno dei fogli di calcolo per le celle con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{< /tab >}}
{{< /tabs >}}
