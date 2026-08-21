---
title: Spaltendetails abrufen – Aspose.Cells Cloud API-Referenz (v4.0)
description: Rufen Sie detaillierte Informationen zu einer Arbeitsblattspalte (Index, Breite, Stil, ausgeblendeter Status) mithilfe der Aspose.Cells Cloud REST-API ab.
keywords: Aspose.Cells, Cloud-API, Excel-Spalte, Spalte abrufen, REST-API, JWT, Arbeitsblatt
date: 2026-07-30
---

# Spaltendetails abrufen  

Rufen Sie detaillierte Informationen zu einer bestimmten Arbeitsblattspalte (Index, Breite, Stil, ausgeblendeter Status) aus einer Excel-Arbeitsmappe ab, die in Aspose Cloud gespeichert ist.

## Inhaltsverzeichnis
1. [Voraussetzungen](#voraussetzungen)  
2. [Authentifizierung](#authentifizierung)  
3. [Endpunkt](#endpunkt)  
4. [Anforderungsparameter](#anforderungsparameter)  
5. [cURL-Beispiel](#curl-beispiel)  
6. [Antwortbeispiel](#antwortbeispiel)  
7. [Antwortschema](#antwortschema)  
8. [Mögliche Fehler](#mögliche-fehler)  
9. [SDK-Beispiele](#sdk-beispiele)  
10. [Zusätzliche Ressourcen](#zusätzliche-ressourcen)  

---

## Voraussetzungen
- Ein gültiges **JWT-Access-Token**, das über die Aspose Cloud-Authentifizierung erhalten wurde.  
- Die Arbeitsmappendatei muss in Aspose Cloud Storage (oder einem anderen unterstützten Speicher) gespeichert sein, und der Ordnerpfad (sofern vorhanden) muss bekannt sein.  

---

## Authentifizierung
Alle Aspose.Cells Cloud APIs verwenden eine **JWT-Token-basierte Authentifizierung**. Geben Sie das Token im `Authorization`-Header an:

```http
Authorization: Bearer <access_token>
```

Einzelheiten zum Erhalten eines Tokens finden Sie im [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Endpunkt
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – Name der Arbeitsmappendatei (z. B. `test.xlsx`).  
- **{sheetName}** – Name des Arbeitsblatts (z. B. `Sheet1`).  
- **{columnIndex}** – nullbasierter Index der abzurufenden Spalte.

---

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## Anforderungsparameter

| Name          | Location | Type    | Erforderlich | Beschreibung |
|---------------|----------|---------|------------|-------------|
| **name**      | path     | string  | Ja         | Name der Arbeitsmappendatei. |
| **sheetName** | path     | string  | Ja         | Arbeitsblatt, das die Spalte enthält. |
| **columnIndex** | path  | integer | Ja         | Nullbasierter Index der abzurufenden Spalte. |
| **folder**    | query    | string  | Nein       | Speicherordner, in dem sich die Arbeitsmappe befindet. |
| **storageName** | query  | string  | Nein       | Name des Speicherdienstes (z. B. Aspose Cloud Storage). |

---

## cURL-Beispiel
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Antwortbeispiel
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Antwortschema
| Feld                 | Type    | Beschreibung |
|----------------------|---------|-------------|
| `Column.GroupLevel`  | integer | Gliederungsebene der Spalte (wird für Gruppierungen verwendet). |
| `Column.Index`       | integer | Nullbasierter Index der Spalte. |
| `Column.IsHidden`    | boolean | `true`, wenn die Spalte ausgeblendet ist; andernfalls `false`. |
| `Column.Width`       | number  | Breite der Spalte in Zeichen. |
| `Column.Style`       | object  | Enthält einen `link` zur Ressource des Spaltenstils. |
| `Column.link`        | object  | Eigenlink zur Spaltenressource. |
| `Code`               | integer | HTTP-Statuscode der Antwort. |
| `Status`             | string  | Textuelle Beschreibung des Status (z. B. **OK**). |

---

## Mögliche Fehler
| HTTP-Status | Code | Nachricht              | Eintrittsgrund |
|-------------|------|------------------------|----------------|
| 400         | 400  | Bad Request            | Fehlende oder fehlerhafte erforderliche Parameter. |
| 401         | 401  | Unauthorized           | Fehlender oder ungültiger `Authorization`-Header. |
| 404         | 404  | Not Found              | Arbeitsmappe, Arbeitsblatt oder Spalte existiert nicht. |
| 500         | 500  | Internal Server Error  | Unerwartetes serverseitiges Problem. |

### Beispiel – 404 Not Found
```json
{
  "Code": 404,
  "Message": "Spaltenindex außerhalb des gültigen Bereichs."
}
```

### Beispiel – 401 Unauthorized
```json
{
  "Code": 401,
  "Message": "Ungültiges oder fehlendes Authentifizierungstoken."
}
```

---

## SDK-Beispiele
Die folgenden Code-Snippets zeigen, wie der Vorgang **Get Worksheet Columns** mithilfe der offiziellen Aspose.Cells Cloud SDKs aufgerufen wird. Falls ein Gist nicht mehr verfügbar ist, ist der Beispielcode direkt enthalten.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// API-Client konfigurieren
var apiInstance = new CellsApi("client_id", "client_secret");

// Erforderliche Parameter festlegen
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // optional
string storageName = "MyStorage";    // optional

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Spaltenindex: " + response.Column.Index);
    Console.WriteLine("Breite: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Ausnahme beim Aufruf von CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // optional
        String storageName = "MyStorage";    // optional

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Spaltenindex: " + result.getColumn().getIndex());
            System.out.println("Breite: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Ausnahme beim Aufruf von CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # optional
storage_name = "MyStorage"  # optional

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Spaltenindex:", response.column.index)
    print("Breite:", response.column.width)
except Exception as e:
    print("Ausnahme beim Aufruf von CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // optional
const storageName = "MyStorage"; // optional

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Spaltenindex:", result.column?.index);
        console.log("Breite:", result.column?.width);
    })
    .catch((error) => {
        console.error("Fehler beim Aufruf von getWorksheetColumns:", error);
    });
```

</details>

> **Hinweis:** Alle SDKs übernehmen den `Authorization`-Header automatisch, sobald Sie `client_id` und `client_secret` bereitstellen.

---

## Zusätzliche Ressourcen
- **OpenAPI-Spezifikation:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **Authentifizierungsleitfaden:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **GitHub-Repository (SDKs & Beispiele):** <https://github.com/aspose-cells-cloud>  

--- 

*Dieses Dokument wurde zuletzt am 2026‑07‑30 aktualisiert.*  
---