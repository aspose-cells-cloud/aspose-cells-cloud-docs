---
title: "Importa dati JSON in Excel"
second_title: "Documento"
linktitle: "Importa JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, importazione JSON, API Excel, importazione REST JSON, esempi SDK"
description: "Scopri come importare dati JSON in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include dettagli endpoint, esempi di richiesta/risposta e codice SDK per .NET, Java e Python."
weight: 40
---

Questa API REST **importa dati JSON** in un foglio di lavoro Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome del parametro    | Posizione     | Tipo   | Descrizione                                                                                          |
| --------------------- | -------------| ------ | ---------------------------------------------------------------------------------------------------- |
| name                  | Path         | string | Nome del file del foglio di calcolo.                                                                 |
| importJsonRequest     | Corpo HTTP   | class  | Payload della richiesta contenente i dettagli dell'importazione JSON.                               |
| password              | Stringa query| string | Password per aprire il foglio di calcolo (se protetto).                                             |
| folder                | Stringa query| string | Cartella contenente il foglio di calcolo originale.                                                 |
| storageName           | Stringa query| string | Nome dell'archiviazione in cui risiede il foglio di calcolo.                                        |
| outPath               | Stringa query| string | Percorso del file di output dopo l'importazione. Se omesso, il foglio di calcolo aggiornato viene restituito nella risposta. |
| outStorageName        | Stringa query| string | Nome dell'archiviazione per il file di output.                                                      |
| checkExcelRestriction | Stringa query| string | Flag che indica se applicare le restrizioni specifiche di Excel (true/false).                      |

### **Esempio di corpo della richiesta**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### Risposta

Una richiesta riuscita restituisce **HTTP 200** con un payload JSON simile al seguente:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codici di stato possibili:

| Codice | Significato                                             |
| ------ | ------------------------------------------------------- |
| 200    | Importazione riuscita                                   |
| 400    | Richiesta non valida – dati mancanti o non validi       |
| 401    | Non autorizzato – token non valido o mancante           |
| 500    | Errore interno del server                               |


## Come utilizzare l'API PostWorkbookImportJson con gli SDK

### Specifica dell'API PostWorkbookImportJson

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più efficiente per velocizzare lo sviluppo. Gli SDK gestiscono i dettagli a basso livello, permettendoti di concentrarti sulla logica di business. Per un elenco completo degli SDK di Aspose.Cells Cloud, visita il [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

---