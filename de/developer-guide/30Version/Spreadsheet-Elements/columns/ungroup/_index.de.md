---
title: Spaltengruppierung in Excel aufheben – Aspose.Cells Cloud API  
description: Entfernen der Spaltengruppierung in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält Endpunkt, Parameter, Authentifizierung, cURL-Beispiel, Antwortformat und SDK-Snippets.  
keywords: Aspose.Cells, Gruppierung aufheben, Spalten, Excel, API, REST, Cloud, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---

# Spaltengruppierung in Excel aufheben  

Aspose.Cells Cloud bietet eine **POST**-Operation zum Entfernen der Spaltengruppierung aus einem angegebenen Arbeitsblatt. Diese Seite beschreibt das Anforderungsformat, die erforderlichen Parameter, die Authentifizierungsmethode, Beispielaufrufe und die SDK-Nutzung.

---  

## Voraussetzungen  

| Anforderung | Warum erforderlich |
|------------|-------------------|
| **Aspose Cloud-Konto** | Zugriff auf die Aspose.Cells Cloud-Dienste. |
| **JWT-Zugriffstoken** | Alle API-Aufrufe müssen mit einem Bearer-Token autorisiert werden. Siehe [JWT-Authentifizierungsanleitung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Arbeitsmappe in Aspose Cloud-Speicher gespeichert** | Die API arbeitet mit Dateien, die sich im Cloud-Speicher (oder in einem verbundenen externen Speicher) befinden. |
| **Arbeitsblattname** | Das Ziel-Arbeitsblatt muss in der Arbeitsmappe vorhanden sein. |

---  

## Authentifizierung  

Alle Anforderungen erfordern einen **Authorization**-Header mit einem gültigen JWT-Token:

```http
Authorization: Bearer <access_token>
```

Das Token wird über den Aspose Cloud OAuth-Flow abgerufen. Token sind zeitlich begrenzt gültig; aktualisieren Sie sie bei Bedarf.

---  

## Endpunkt  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Pfad** – Name der Arbeitsmappendatei (z. B. `test.xlsx`).  
* `{sheetName}` – **Pfad** – Name des Arbeitsblatts (z. B. `Sheet1`).  

---  

## Parameter  

### Pfadparameter  

| Name | Typ | Erforderlich | Beschreibung |
|------|-----|--------------|-------------|
| `name` | string | Ja | Name der Arbeitsmappendatei. |
| `sheetName` | string | Ja | Name des Arbeitsblatts. |

### Abfrageparameter  

| Name | Typ | Erforderlich | Beschreibung |
|------|-----|--------------|-------------|
| `firstIndex` | integer | Ja | Nullbasierter Index der ersten Spalte, deren Gruppierung aufgehoben werden soll. |
| `lastIndex` | integer | Ja | Nullbasierter Index der letzten Spalte, deren Gruppierung aufgehoben werden soll. |
| `folder` | string | Nein | Ordnerpfad, der die Arbeitsmappe enthält. |
| `storageName` | string | Nein | Name des Speicherdiensts, in dem sich die Datei befindet. |

---  

## Anforderungsbeispiel (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*Ersetzen Sie `<access_token>` durch ein gültiges JWT-Token.*

---  

## Erfolgreiche Antwort  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

Das Antwortobjekt (`CellsCloudResponse`) enthält den Bereich der Spalten, deren Gruppierung erfolgreich aufgehoben wurde.

### Fehlerantwort  

Bei einem fehlgeschlagenen Aufruf gibt der Dienst eine JSON-Payload mit folgenden Feldern zurück:

| Feld | Bedeutung |
|------|-----------|
| `Code` | HTTP-ähnlicher Fehlercode (z. B. 400, 401). |
| `Status` | Kurzbeschreibung des Fehlers. |
| `ErrorMessage` | Detaillierte Fehlerbeschreibung. |

---  

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |
---  

## SDK-Codebeispiele  

Im Folgenden finden Sie sofort ausführbare Codeausschnitte für die gängigsten SDKs. Ersetzen Sie Platzhalterwerte (`<YourAccessToken>`, `<YourFileName>` usw.) durch Ihre eigenen Daten.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Gruppierung aufgehoben für Spalten: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Gruppierung aufgehoben für Spalten: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Gruppierung aufgehoben für Spalten: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Gruppierung aufgehoben für Spalten: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Gruppierung aufgehoben für Spalten: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **Hinweis:** SDKs für PHP, Ruby, Perl und andere Sprachen folgen derselben Parameterreihenfolge. Vollständige Beispiele finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

---  

## Referenzen  

* **OpenAPI-Spezifikation:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Authentifizierungsanleitung:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **SDK-Repository:** <https://github.com/aspose-cells-cloud>

---  

## Versionshistorie  

| Datum | Autor | Änderung |
|-------|-------|----------|
| 2026‑07‑30 | AI Optimizer | UTF‑8-Kodierung korrigiert, Voraussetzungen hinzugefügt, Metadaten-Keywords bereinigt, Überschriftenhierarchie verbessert, SDK-Snippets eingefügt. |
| 2026‑07‑29 | Original | Erster Entwurf der Dokumentation. |

---