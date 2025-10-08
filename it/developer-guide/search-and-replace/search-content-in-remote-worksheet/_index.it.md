---
title: Aspose.Cells Cloud Web API - Cerca il contenuto del foglio di lavoro nel foglio di calcolo remoto
second_title: Documen
ArticleTitle: Search Worksheet Content in Remote Spreadshee
linktitle: Cerca il contenuto del foglio di lavoro remoto
type: docs
url: /it/search-content-in-remote-worksheet/
keywords: Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet AP
description: Cerca in modo efficiente il testo all'interno di un foglio di lavoro di un foglio di calcolo remoto archiviato nel cloud
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Trova tutte le celle vuote in un foglio di lavoro Excel, Ricerca foglio di lavoro remoto
---
Cerca un testo specificato all'interno di un foglio di lavoro di un foglio di calcolo remoto archiviato nel cloud.

## **Dettagli dell'interfaccia**

## **Cerca contenuto nel foglio di lavoro remoto**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|nome|Corda|Sentiero|Nome del file della cartella di lavoro da cercare.|
|foglio di lavoro|Corda|Sentiero|Il nome del foglio di lavoro.|
|testo di ricerca|Corda|Domanda|Il testo da ricercare.|
|ignorando il caso|Booleano|Domanda|Indica se ignorare la distinzione tra maiuscole e minuscole durante la ricerca.|
|cartella|Corda|Domanda|Percorso della cartella in cui è archiviata la cartella di lavoro.|
|Nome di archiviazione|Corda|Domanda|(Facoltativo) Il nome dell'archiviazione se si utilizza un archivio cloud personalizzato. Se omesso, viene utilizzato l'archivio predefinito.|
|regione|Corda|Domanda|Impostazione della regione del foglio di calcolo.|
|password|Corda|Domanda|La password per aprire il file del foglio di calcolo.|

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

## Dove dovremmo utilizzare il contenuto di ricerca all'interno del foglio di lavoro del foglio di calcolo API?

Quando hai bisogno di cercare contenuti all'interno del foglio di lavoro di Spreadsheet, puoi utilizzare questo API.

## Perché dovresti usare il contenuto di Ricerca all'interno del foglio di lavoro del Foglio di calcolo API?

- Cerca senza sforzo i contenuti all'interno di un foglio di calcolo remoto con questo API.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la ricerca di collegamenti interrotti all'interno del foglio di lavoro del foglio di calcolo API con SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) definisce un'interfaccia di programmazione accessibile al pubblico e consente interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice i contenuti di ricerca all'interno di fogli di lavoro o fogli di calcolo per celle, con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come chiamare i servizi Web Aspose.Cells utilizzando vari SDK:
