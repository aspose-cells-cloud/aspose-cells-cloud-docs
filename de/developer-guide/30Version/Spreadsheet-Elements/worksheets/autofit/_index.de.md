---
title: "Arbeiten mit AutoAnpassung in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "AutoAnpassung"
type: docs
url: /worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "AutoAnpassung, Spalte, Zeile, Aspose.Cells, Cloud, Excel, API, Größe anpassen"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API Spalten und Zeilen in einem Excel-Arbeitsblatt automatisch anpassen. Enthält Beispiele für cURL, .NET, Java und Python."
weight: 20
ArticleTitle: "Arbeiten mit AutoAnpassung in einem Excel-Arbeitsblatt – Aspose.Cells Cloud API"
---

## Arbeiten mit AutoAnpassung in einem Excel-Arbeitsblatt

- [So passen Sie eine Spalte in einem Excel-Arbeitsblatt automatisch an.](/cells/worksheets/autofit/column/)
- [So passen Sie mehrere Spalten in einem Excel-Arbeitsblatt automatisch an.](/cells/worksheets/autofit/columns/)
- [So passen Sie eine Zeile in einem Excel-Arbeitsblatt automatisch an.](/cells/worksheets/autofit/row/)
- [So passen Sie mehrere Zeilen in einem Excel-Arbeitsblatt automatisch an.](/cells/worksheets/autofit/rows/)

**Voraussetzungen**  
Bevor Sie die AutoAnpassungs-Operationen verwenden können, benötigen Sie Folgendes:

1. Ein Aspose.Cells Cloud-Konto mit gültiger **Client-ID** und **Client-Geheimnis**.  
2. Eine Arbeitsmappe, die in Aspose Cloud-Speicher hochgeladen wurde (oder über eine öffentliche URL erreichbar ist).  
3. Der Name des Arbeitsblatts, das Sie ändern möchten.

**API-Referenz**  

| Operation | HTTP-Methode | Endpunkt | Erforderliche Parameter | Anforderungstext | Beispiel-Antwort | Statuscodes |
|-----------|-------------|----------|--------------------|--------------|----------------|--------------|
| Spalte automatisch anpassen (**column**) | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (Pfad) <br> `columnIndex` (Abfrage) | *keine* | `{ "code": 200, "status": "OK", "message": "Spalte automatisch angepasst." }` | 200, 400, 401, 404, 500 |
| Mehrere Spalten automatisch anpassen (**columns**) | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (Pfad) <br> `startColumn`, `endColumn` (Abfrage) | *keine* | `{ "code": 200, "status": "OK", "message": "Spalten automatisch angepasst." }` | 200, 400, 401, 404, 500 |
| Zeile automatisch anpassen (**row**) | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (Pfad) <br> `rowIndex` (Abfrage) | *keine* | `{ "code": 200, "status": "OK", "message": "Zeile automatisch angepasst." }` | 200, 400, 401, 404, 500 |
| Mehrere Zeilen automatisch anpassen (**rows**) | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (Pfad) <br> `startRow`, `endRow` (Abfrage) | *keine* | `{ "code": 200, "status": "OK", "message": "Zeilen automatisch angepasst." }` | 200, 400, 401, 404, 500 |

**Codebeispiele**

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

// Authentifizierung
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// AutoAnpassung für Spalten aufrufen
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

// AutoAnpassung für Zeilen
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

# AutoAnpassung für eine einzelne Spalte
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

Diese Code-Snippets demonstrieren, wie Sie:

1. Sich mit Aspose.Cells Cloud anhand Ihrer **Client-ID** und **Client-Geheimnis** authentifizieren.  
2. Den entsprechenden AutoAnpassungs-Endpunkt für Spalten oder Zeilen aufrufen.  
3. Die Antwort verarbeiten, die bestätigt, dass der Vorgang erfolgreich war.

**Nächste Schritte**

Nach Abschluss des AutoAnpassungs-Aufrufs können Sie die aktualisierte Arbeitsmappe herunterladen:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

Sie können die Parameter `startColumn`, `endColumn`, `startRow` und `endRow` problemlos anpassen, um gezielt bestimmte Bereiche zu erfassen.
---