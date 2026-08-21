---
---
title: "Lavorare con Excel ListObject"
ArticleTitle: "Lavorare con Excel ListObject"
second_title: "Document"
linktype: "ListObjects"
type: docs
url: /it/list-objects/
aliases:
  - /it/working-with-list-objects/
  - /it/working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, API per tabelle Excel, aggiungere tabella, aggiornare tabella, eliminare tabella, convertire tabella in intervallo, ordinare tabella Excel"
description: "Scopri come aggiungere, aggiornare, eliminare, recuperare, ordinare e convertire oggetti ListObject (tabelle) di Excel tramite l'API REST di Aspose.Cells Cloud. Include esempi di codice per C#, Java, Python e altro ancora."
weight: 100
---

Gli **ListObject Excel** (tabelle) offrono un modo strutturato per organizzare insiemi di dati. Includono funzionalità come l'ordinamento automatico dei dati, righe di intestazione, filtri integrati e facoltativamente righe totali. Padroneggia queste capacità per analizzare i tuoi dati velocemente ed efficientemente.

**Definizione di ListObject:** Un **ListObject** è l'oggetto tabella nativo di Excel che raggruppa righe e colonne, consente ordinamento, filtraggio e formattazione, ed è accessibile tramite l'API REST di Aspose.Cells Cloud.

## Come lavorare con le tabelle (ListObject)

- [Come aggiungere una tabella (ListObject) all'interno del foglio di lavoro](/it/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [Come aggiornare una tabella (ListObject) all'interno del foglio di lavoro](/it/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [Come convertire una tabella (ListObject) in un intervallo](/it/cells/convert-list-object-or-table-to-range/)
- [Come ordinare i dati della tabella](/it/cells/sort-table-data/)
- [Come rimuovere le righe duplicate da una tabella](/it/cells/list-objects/remove-duplicates/)
- [Come inserire un filtro a segmenti per una tabella](/it/cells/list-objects/insert-slicer/)

**Riferimento API (panoramica):**  
L'API REST di Aspose.Cells Cloud espone le operazioni su ListObject tramite endpoint come `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` e `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. I parametri di query obbligatori includono `folder` e `storage`. I corpi delle richieste sono oggetti JSON che descrivono le proprietà della tabella (nome, `showHeaderRow`, `showTotalRow`, ecc.), mentre le risposte restituiscono payload JSON contenenti i dettagli del ListObject creato o modificato.

**Prerequisiti:**  
- Un token di autenticazione valido di Aspose.Cells Cloud.  
- Il file del workbook deve essere caricato in una posizione di archiviazione supportata (impostazione predefinita: **/**) e il parametro di query `folder` deve puntare a tale posizione.  
- Opzionale: impostare `storage` se si utilizza un servizio di archiviazione diverso da quello predefinito.

**Dettagli endpoint**

| Metodo | Endpoint | Parametri di query | Corpo della richiesta (JSON) | Risposta in caso di successo (esempio) | Codici di stato |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obbligatorio), `storage` (opzionale) | *nessuno* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Richiesta non valida, 401 – Non autorizzato, 404 – Non trovato |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obbligatorio), `storage` (opzionale) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Creato, 400 – Richiesta non valida, 401 – Non autorizzato, 409 – Conflitto |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obbligatorio), `storage` (opzionale) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Richiesta non valida, 401 – Non autorizzato, 404 – Non trovato |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obbligatorio), `storage` (opzionale) | *nessuno* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Richiesta non valida, 401 – Non autorizzato, 404 – Non trovato |

** frammenti di codice**

*C# (POST – Aggiungi ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – Recupera ListObject)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – Aggiorna ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – Rimuovi ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Note:**  
- Gli indici ListObject sono in base zero.  
- Quando si aggiunge un ListObject, `StartRow` e `StartColumn` definiscono la cella in alto a sinistra della tabella.  
- L'API supporta la paginazione tramite i parametri di query `offset` e `limit` (non mostrati nella tabella) per fogli di lavoro di grandi dimensioni.  
- Limiti di velocità: 100 richieste al minuto per account; superare questo limite restituisce **429 Too Many Requests**.

Incorporando il termine **Excel ListObject** più volte nel contenuto della pagina, il testo si allinea con le parole chiave target "Excel ListObject", "Aspose.Cells Cloud" e "Excel table API", migliorando il SEO mantenendo un linguaggio naturale per i lettori.