---
title: Aspose.Cells Cloud Web API - Sostituisci il contenuto nel foglio di calcolo remoto
second_title: Documen
ArticleTitle: Replace Content in Remote a Spreadshee
linktitle: Sostituisci il contenuto del foglio di calcolo remoto
type: docs
url: /it/replace-content-in-remote-spreadsheet/
keywords: Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacemen
description: Sostituisci in modo efficiente il testo nei fogli di calcolo remoti utilizzando Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Sostituisci contenuto in Excel, Sostituzione testo basata su cloud, Modifica testo in foglio di calcolo remoto
---
Sostituisci in modo efficiente il testo specificato all'interno di un file di foglio di calcolo remoto.

## **Sostituisci contenuto nel foglio di calcolo remoto API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| nome| Corda| Sentiero| Nome del file della cartella di lavoro da modificare.|
| testo di ricerca| Corda| Domanda| Il testo da cercare nel foglio di calcolo.|
| sostituisciTesto| Corda| Domanda| Il testo per sostituire le occorrenze trovate.|
| cartella| Corda| Domanda| Percorso della cartella in cui è archiviata la cartella di lavoro.|
| Nome di archiviazione| Corda| Domanda|(Facoltativo) Il nome dell'archivio se si utilizza un archivio cloud personalizzato. Se omesso, utilizzare l'archivio predefinito.|
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

## Dove dovremmo usare il contenuto Sostituisci nel foglio di calcolo remoto API?

Quando è necessario sostituire il contenuto in un foglio di calcolo remoto, è possibile utilizzare questo API.

## Perché dovresti usare la funzione Sostituisci contenuto nel foglio di calcolo remoto API?

- Sostituisci rapidamente i contenuti nei fogli di calcolo remoti.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la funzione Sostituisci contenuto nel foglio di calcolo remoto API con SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice la sostituzione del contenuto nelle celle dei fogli di calcolo con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
