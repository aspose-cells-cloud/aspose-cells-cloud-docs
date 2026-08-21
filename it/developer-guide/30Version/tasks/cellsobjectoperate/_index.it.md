---
---
title: "Aspose.Cells Cloud API – Lavorare con l'attività CellsObjectOperate (REST)"
second_title: "Document"
type: docs
url: /it/tasks/cells-object-operate/
aliases: [/it/working-with-cellsobjectoperate-task/]
description: "Scopri come utilizzare l'attività CellsObjectOperate nell'API Aspose.Cells Cloud, con riferimento ai parametri, esempi di richiesta/risposta e consigli pratici per fogli di calcolo, grafici e tabelle pivot."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – Lavorare con l'attività CellsObjectOperate (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "attività CellsObjectOperate"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "operazione su grafico"
  - "API per tabelle pivot"
  - "API per interruzioni di pagina"
---

**Panoramica**  
L'attività **CellsObjectOperate** consente di eseguire operazioni di creazione, lettura, aggiornamento ed eliminazione (CRUD) su oggetti Excel come cartelle di lavoro, fogli di calcolo, grafici, tabelle pivot, forme, interruzioni di pagina e altri ancora, tramite una singola chiamata REST. Specificare il tipo di oggetto con `OperateObjectType` e fornire il blocco di parametri corrispondente (ad esempio, `ChartOperateParameter` per azioni relative ai grafici).

---

**OperateObject**

| Nome parametro          | Tipo   | Descrizione |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | Il tipo di oggetto Excel su cui eseguire l'operazione. Valori ammessi: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition   | object | Contenitore che identifica la posizione dell'oggetto target (ad esempio, nome della cartella di lavoro, nome del foglio di calcolo, indice del grafico). Richiesto per la maggior parte delle operazioni. |

**OperateObjectPosition**

| Nome parametro | Tipo   | Descrizione |
| -------------- | ------ | ----------- |
| Workbook       | object | La cartella di lavoro contenente l'oggetto target. Deve includere uno tra `FileName` (archivio cloud) o `FileContent` (codificato in base‑64). |
| SheetName      | string | Nome del foglio di calcolo su cui viene applicata l'operazione. Richiesto per oggetti a livello di foglio (grafici, forme, ecc.). |
| ChartIndex     | integer| Indice in base zero del grafico all'interno del foglio di calcolo (utilizzato quando `OperateObjectType` è `Chart`). |
| ShapeIndex     | integer| Indice in base zero della forma all'interno del foglio di calcolo (utilizzato quando `OperateObjectType` è `Shape`). |
| CellName       | string | Riferimento alla cella in stile A1 (ad esempio, `A1`). Utilizzato per operazioni a livello di cella. |
| ListObjectIndex| integer| Indice in base zero dell'oggetto elenco (utilizzato quando `OperateObjectType` è `ListObject`). |

**ChartOperateParameter**

| Nome parametro        | Tipo    | Descrizione |
| --------------------- | ------- | ----------- |
| ChartIndex            | integer | Indice del grafico da modificare. Richiesto quando si aggiorna un grafico esistente. |
| ChartType             | string  | Tipo di grafico da creare (ad esempio, `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | integer | Numero di riga dell'angolo superiore sinistro del grafico (in base zero). |
| UpperLeftColumn       | integer | Numero di colonna dell'angolo superiore sinistro del grafico (in base zero). |
| LowerRightRow         | integer | Numero di riga dell'angolo inferiore destro del grafico. |
| LowerRightColumn      | integer | Numero di colonna dell'angolo inferiore destro del grafico. |
| Area                  | string  | Intervallo di dati per il grafico (ad esempio, `A1:B5`). |
| IsVertical            | string  | `true` se l'orientamento del grafico è verticale; altrimenti `false`. |
| CategoryData          | string  | Intervallo che fornisce le etichette dell'asse X (categorie). |
| IsAutoGetSerialName   | string  | `true` per generare automaticamente i nomi delle serie; `false` per utilizzare nomi personalizzati. |
| Title                 | string  | Testo del titolo visualizzato nel grafico. |

**ListObjectOperateParameter**

| Nome parametro | Tipo   | Descrizione |
| -------------- | ------ | ----------- |
| ListObject     | object | Oggetto di configurazione per un'operazione sull'elenco (tabella). Include proprietà come `ShowHeader`, `ShowTotal` e `Style`. |

**PageBreakOperateParameter**

| Nome parametro | Tipo    | Descrizione |
| -------------- | ------- | ----------- |
| PageBreakType  | string  | Tipo di interruzione di pagina (`Horizontal` o `Vertical`). |
| Index          | integer | Indice in base zero dell'interruzione di pagina da eliminare o modificare. |
| Row            | integer | Numero di riga in cui inserire un'interruzione di pagina orizzontale. |
| Column         | integer | Numero di colonna in cui inserire un'interruzione di pagina verticale. |
| StartIndex     | integer | Indice iniziale per un'operazione su intervallo di interruzioni di pagina. |
| EndIndex       | integer | Indice finale per un'operazione su intervallo di interruzioni di pagina. |

**PageSetupOperateParameter**

| Nome parametro | Tipo   | Descrizione |
| -------------- | ------ | ----------- |
| PageSetup      | object | Impostazioni per il layout di pagina (margini, orientamento, dimensione carta, ecc.). |

**PivotTableOperateParameter**

| Nome parametro   | Tipo        | Descrizione |
| ---------------- | ----------- | ----------- |
| DestCellName     | string      | Cella in alto a sinistra dell'intervallo di destinazione per la tabella pivot (ad esempio, `C5`). |
| SourceData       | string      | Intervallo di origine della tabella pivot (ad esempio, `A1:D100`). |
| TableName        | string      | Nome assegnato alla tabella pivot creata. |
| UseSameSource    | string      | `true` per riutilizzare un intervallo di origine esistente; `false` per crearne uno nuovo. |
| PivotTableIndex  | integer     | Indice della tabella pivot da aggiornare (richiesto per azioni di modifica/eliminazione). |
| PivotFieldRows   | integer[]   | Raccolta di indici di campi che appariranno nell'area righe. |
| PivotFieldColumns| integer[]   | Raccolta di indici di campi che appariranno nell'area colonne. |
| PivotFieldData   | integer[]   | Raccolta di indici di campi che appariranno nell'area dati. |

**ShapeOperateParameter**

| Nome parametro | Tipo   | Descrizione |
| -------------- | ------ | ----------- |
| Shape          | object | Definizione della forma (tipo, posizione, dimensione, testo, ecc.). |

**WorkbookSettingsOperateParameter**

| Nome parametro   | Tipo   | Descrizione |
| ---------------- | ------ | ----------- |
| WorkbookSettings | object | Impostazioni che influenzano l'intera cartella di lavoro (ad esempio, modalità di calcolo, precisione). |

**WorksheetOperateParameter**

| Nome parametro | Tipo   | Descrizione |
| -------------- | ------ | ----------- |
| Name           | string | Nome corrente del foglio di calcolo su cui eseguire l'operazione. |
| SheetType      | string | Tipo di foglio (`Worksheet`, `Chart`, ecc.). |
| NewName        | string | Nuovo nome per il foglio di calcolo durante la ridenominazione. |
| MovingRequest  | object | Parametri per spostare un foglio di calcolo (ad esempio, `FromIndex`, `ToIndex`). |

## API REST

| API                | Tipo | Descrizione | Link alla risorsa |
| ------------------ | ---- | ----------- | ----------------- |
| /cells/task/runtask| POST | Esegui attività | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

### Prerequisiti
- **Autenticazione** – Includere l'intestazione `Authorization: Bearer <access_token>` con un token valido.  
- **Archivio** – La cartella di lavoro di origine deve essere memorizzata in Aspose Cloud Storage oppure fornita come contenuto codificato in base‑64 nel corpo della richiesta.  
- **Versione API** – Questa documentazione fa riferimento alla **v3.0** dell'API Aspose.Cells Cloud.

### Esempio di richiesta (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Grafico Vendite",
               "IsVertical": "true"
           }
         }'
```

Il corpo della richiesta segue lo schema **CellsObjectOperateRequest** definito di seguito:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* Altre definizioni omesse per brevità */
  }
}
```

### Esempio di risposta (esito positivo – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Grafico creato correttamente."
  }
}
```

La risposta contiene i seguenti campi:

| Campo   | Tipo   | Descrizione |
| ------- | ------ | ----------- |
| Code    | integer| Codice di stato simile a HTTP restituito dall'engine dell'attività. |
| Status  | string | Stato leggibile dall'uomo (ad esempio, `OK`). |
| TaskId  | string | Identificativo dell'attività asincrona. |
| Result  | object | Oggetto contenente i risultati specifici dell'operazione. |
| Result.ChartId | integer | Identificativo del grafico creato o modificato. |
| Result.Message | string | Messaggio breve che descrive l'esito. |

### Gestione degli errori

| Stato HTTP | Codice errore | Descrizione | Rimedio consigliato |
| ---------- | ------------- | ----------- | ------------------- |
| 400        | InvalidParameter | Uno o più parametri di richiesta mancano o sono formattati in modo errato. | Verificare i campi obbligatori e i tipi di dato. |
| 401        | Unauthorized   | Token di autenticazione non valido o mancante. | Aggiornare il token di accesso e includerlo nell'intestazione `Authorization`. |
| 404        | NotFound       | La cartella di lavoro, il foglio di calcolo o l'oggetto specificati non esistono. | Verificare `FileName`, `SheetName` e gli indici degli oggetti. |
| 500        | ServerError    | Si è verificato un errore imprevisto sul server. | Riprovare la richiesta; se il problema persiste, contattare il supporto. |

### Casi d’uso comuni
- **Aggiungere un nuovo grafico** a un foglio di calcolo.  
- **Ridenominare un foglio di calcolo** (`OperateObjectType = "Worksheet"` con `WorksheetOperateParameter.NewName`).  
- **Inserire un'interruzione di pagina** (`OperateObjectType = "PageBreak"` con `PageBreakOperateParameter`).  
- **Aggiornare i dati di origine di una tabella pivot** (`OperateObjectType = "PivotTable"` con `PivotTableOperateParameter.SourceData`).  
- **Modificare le impostazioni della cartella di lavoro**, come la modalità di calcolo (`OperateObjectType = "WorkbookSettings"`).  

---  

*Le seguenti descrizioni sono tratte dalla specifica ufficiale Aspose.Cells Cloud OpenAPI.*
---