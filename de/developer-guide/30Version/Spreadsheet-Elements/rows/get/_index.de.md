---
---
title: "Abrufen einer einzelnen Zeile aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API"
description: "Erfahren Sie, wie Sie eine bestimmte Zeile aus einem Excel-Arbeitsblatt abrufen, das im Aspose Cloud Storage gespeichert ist, mithilfe der Aspose.Cells Cloud REST API. Enthält die Anforderungssyntax, Parameter, Antwortschema, ein cURL-Beispiel und SDK-Code (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, Zeile abrufen, Excel API, Tabellenkalkulation REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# Abrufen einer einzelnen Zeile aus einem Excel-Arbeitsblatt

**Endpoint**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Ruft eine Zeile aus einem Arbeitsblatt ab, das im Aspose Cloud Storage gespeichert ist. Für diesen Vorgang ist ein gültiger OAuth 2.0-Zugriffstoken mit dem Scope **Read** erforderlich.

---

## Inhaltsverzeichnis
1. [Voraussetzungen](#voraussetzungen)  
2. [HTTP-Anforderung](#http-anforderung)  
3. [Parameter](#parameter)  
   - [Pfadparameter](#pfadparameter)  
   - [Abfrageparameter](#abfrageparameter)  
4. [cURL-Beispiel](#curl-beispiel)  
5. [Antwort](#antwort)  
   - [Erfolgsschema](#erfolgsschema)  
   - [Statuscodes](#statuscodes)  
6. [SDK-Codebeispiele](#sdk-codebeispiele)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [Verwandte Vorgänge](#verwandte-vorgänge)  
8. [Hinweise & Einschränkungen](#hinweise--einschraenkungen)  

---

## Voraussetzungen
- **Aspose Cloud-Konto** mit aktiver Subscription.  
- **OAuth 2.0-Zugriffstoken** mit dem Scope **Read**.  
- Die Ziel-Arbeitsmappe muss bereits im Aspose Cloud Storage vorhanden sein.  

---

## HTTP-Anforderung
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*Base URL*: `https://api.aspose.cloud/v3.0`

---

## Parameter

### Pfadparameter
| Name      | Type   | Erforderlich | Beschreibung                         |
|-----------|--------|--------------|-------------------------------------|
| `name`    | string | ✅           | Name der Arbeitsmappendatei (z. B. `MeineArbeitsmappe.xlsx`). |
| `sheetName`| string | ✅          | Name des Arbeitsblatts (z. B. `Tabelle1`). |
| `rowIndex`| integer| ✅           | Nullbasiertes Index der abzurufenden Zeile. |

### Abfrageparameter *(optional)*
| Name        | Type   | Erforderlich | Beschreibung |
|-------------|--------|--------------|-------------|
| `folder`    | string | ❌           | Pfad zum Ordner im Cloud-Speicher, in dem sich die Arbeitsmappe befindet. |
| `storageName`| string| ❌           | Name des Speicherdiensts (falls ein benutzerdefinierter Speicher verwendet wird). |

---

## cURL-Beispiel
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MeineArbeitsmappe.xlsx/worksheets/Tabelle1/rows/5?folder=Dokumente&storageName=MeinSpeicher" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Antwort

### Erfolgsschema (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* Stil-Objekt */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...weitere Zellen... */
    ]
  }
}
```

### Statuscodes
| Code | Bedeutung |
|------|-----------|
| **200** | Zeile erfolgreich abgerufen. |
| **401** | Nicht autorisiert – fehlender oder ungültiger Zugriffstoken. |
| **404** | Arbeitsmappe, Arbeitsblatt oder Zeile nicht gefunden. |
| **500** | Interner Serverfehler. |

### Fehlerbeispiel (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Zugriffstoken fehlt oder ist ungültig."
}
```

---

## SDK-Codebeispiele

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "IHR_CLIENT_ID";
var clientSecret = "IHR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MeineArbeitsmappe.xlsx",
    sheetName: "Tabelle1",
    rowIndex: 5,
    folder: "Dokumente",
    storageName: null   // optional
);

Console.WriteLine($"Zeile {response.Row.Index} mit {response.Row.Cells.Count} Zellen abgerufen.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("IHR_CLIENT_ID", "IHR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MeineArbeitsmappe.xlsx",
    "Tabelle1",
    5,
    "Dokumente",
    null   // storageName – optional
);

System.out.println("Zeilenindex: " + response.getRow().getIndex());
System.out.println("Zellanzahl: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "IHR_CLIENT_ID"
client_secret = "IHR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MeineArbeitsmappe.xlsx",
        sheet_name="Tabelle1",
        row_index=5,
        folder="Dokumente",
        storage_name=None
    )
    print(f"Zeile {response.row.index} mit {len(response.row.cells)} Zellen abgerufen.")
except ApiException as e:
    print("Ausnahme beim Aufruf von CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## Verwandte Vorgänge
| Vorgang | Beschreibung |
|---------|-------------|
| **Zeile hinzufügen** | `POST /cells/{name}/worksheets/{sheetName}/rows` – Fügt eine neue Zeile in ein Arbeitsblatt ein. |
| **Zeile löschen** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – Entfernt eine vorhandene Zeile. |
| **Mehrere Zeilen abrufen** | `GET /cells/{name}/worksheets/{sheetName}/rows` – Ruft eine Sammlung von Zeilen ab. |
| **Übersicht über Zeilen** | `/cells/rows/` – Allgemeine Dokumentation zu zeilenbezogenen Endpunkten. |

---

## Hinweise & Einschränkungen
- **Rate-Limit**: 100 Anfragen pro Minute pro Konto.  
- **Unterstützte Formate**: XLS, XLSX, CSV, ODS.  
- Der Zeilenindex ist **nullbasiert**; die erste Zeile hat den Index `0`.  
- Stellen Sie sicher, dass die Arbeitsmappe vor dem Aufruf dieses Endpunkts in den angegebenen `folder` hochgeladen wurde.  

---
---