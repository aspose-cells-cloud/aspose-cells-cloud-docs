---
title: Aspose.Cells Cloud Web API - Sostituisci il contenuto del foglio di lavoro nel foglio di calcolo remoto
second_title: Documen
ArticleTitle: Replace Worksheet Content in Remote a Spreadshee
linktitle: Sostituisci il contenuto del foglio di lavoro remoto
type: docs
url: /it/replace-content-in-remote-worksheet/
keywords: Aspose.Cells Cloud Web API, Replace Content, Remote Worksheet, Cloud Spreadsheet, Text Replacement, Office Cloud Integratio
description: Sostituisci in modo efficiente il testo nel foglio di lavoro di un foglio di calcolo remoto utilizzando Aspose.Cells API
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel, ReplaceContentInRemoteWorksheet
---
Sostituisci in modo efficiente il testo specificato all'interno di un foglio di lavoro di un file di foglio di calcolo remoto.

## **Sostituisci il contenuto nel foglio di lavoro remoto API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| nome| Corda| Sentiero| Nome del file della cartella di lavoro da modificare.|
| foglio di lavoro| Corda| Sentiero| Specificare il foglio di lavoro per la sostituzione.|
| testo di ricerca| Corda| Domanda| Il testo da cercare nel foglio di lavoro.|
| sostituisciTesto| Corda| Domanda| Il testo con cui sostituire il testo cercato.|
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

## Dove dovremmo usare il contenuto Sostituisci del foglio di lavoro nel foglio di calcolo remoto API?

Quando è necessario sostituire il contenuto del foglio di lavoro in un foglio di calcolo remoto, è possibile utilizzare questo API.

## Perché dovresti usare la funzione Sostituisci contenuto del foglio di lavoro nel foglio di calcolo remoto API?

- Sostituisci rapidamente il contenuto del foglio di lavoro nei fogli di calcolo remoti.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la funzione Sostituisci contenuto del foglio di lavoro in Remote Spreadsheet API con SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice la sostituzione del contenuto del foglio di lavoro nei fogli di calcolo per le celle con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:
