---
---
title: "Lavorare con l'adattamento automatico in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Adattamento automatico"
type: docs
url: /it/worksheets/autofit/
aliases: [/it/autofit-rows-and-columns-of-worksheet/]
keywords: "adattamento automatico, colonna, riga, Aspose.Cells, Cloud, Excel, API, ridimensiona"
description: "Scopri come ridimensionare automaticamente righe e colonne in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi in cURL, .NET, Java e Python."
weight: 20
ArticleTitle: "Lavorare con l'adattamento automatico in un foglio di calcolo Excel – Aspose.Cells Cloud API"
---

## Lavorare con l'adattamento automatico in un foglio di calcolo Excel

- [Come adattare automaticamente una colonna in un foglio di calcolo Excel.](/it/cells/worksheets/autofit/column/)
- [Come adattare automaticamente colonne in un foglio di calcolo Excel.](/it/cells/worksheets/autofit/columns/)
- [Come adattare automaticamente una riga in un foglio di calcolo Excel.](/it/cells/worksheets/autofit/row/)
- [Come adattare automaticamente righe in un foglio di calcolo Excel.](/it/cells/worksheets/autofit/rows/)

**Prerequisiti**  
Prima di utilizzare le operazioni di adattamento automatico è necessario disporre di:

1. Un account Aspose.Cells Cloud con un **Client Id** e un **Client Secret** validi.  
2. Un foglio di calcolo caricato su Aspose Cloud Storage (o accessibile tramite un URL pubblico).  
3. Il nome del foglio di calcolo che si intende modificare.

**Riferimento API**  

| Operazione | Metodo HTTP | Endpoint | Parametri obbligatori | Corpo della richiesta | Risposta di esempio | Codici di stato |
|-----------|-------------|----------|--------------------|--------------|----------------|--------------|
| Adatta automaticamente una **colonna** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (path) <br> `columnIndex` (query) | *nessuno* | `{ "code": 200, "status": "OK", "message": "Colonna adattata automaticamente." }` | 200, 400, 401, 404, 500 |
| Adatta automaticamente **colonne** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (path) <br> `startColumn`, `endColumn` (query) | *nessuno* | `{ "code": 200, "status": "OK", "message": "Colonne adattate automaticamente." }` | 200, 400, 401, 404, 500 |
| Adatta automaticamente una **riga** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (path) <br> `rowIndex` (query) | *nessuno* | `{ "code": 200, "status": "OK", "message": "Riga adattata automaticamente." }` | 200, 400, 401, 404, 500 |
| Adatta automaticamente **righe** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (path) <br> `startRow`, `endRow` (query) | *nessuno* | `{ "code": 200, "status": "OK", "message": "Righe adattate automaticamente." }` | 200, 400, 401, 404, 500 |

**Esempi di codice**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Autenticazione
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// Chiamata per adattare automaticamente le colonne
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Adatta automaticamente le righe
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# Adatta automaticamente una singola colonna
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

Questi frammenti di codice dimostrano come:

1. Eseguire l'autenticazione con Aspose.Cells Cloud utilizzando il proprio **Client Id** e **Client Secret**.  
2. Chiamare l'endpoint di adattamento automatico appropriato per colonne o righe.  
3. Elaborare la risposta, che conferma il successo dell'operazione.

**Passaggi successivi**

Dopo il completamento della chiamata di adattamento automatico, è possibile scaricare il foglio di calcolo aggiornato:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

Sentitevi liberi di regolare i parametri `startColumn`, `endColumn`, `startRow` ed `endRow` per mirare a intervalli specifici.
---