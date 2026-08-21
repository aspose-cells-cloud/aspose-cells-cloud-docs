---
title: "Aspose.Cells Cloud API – Listobjekt (Tabelle) aus Arbeitsblatt abrufen"
description: "Rufen Sie ein ListObject (Tabelle) aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API ab. Unterstützt den Export in mehrere Formate (PDF, CSV, JSON, …)."
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Tabelle
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Listobjekt (Tabelle) aus Arbeitsblatt abrufen

Rufen Sie ein **Listobjekt** (auch als *Tabelle* bezeichnet) aus einem bestimmten Arbeitsblatt einer Excel-Arbeitsmappe ab. Der Endpunkt kann die Tabelle auch direkt in ein gewähltes Format exportieren, indem der optionale Abfrageparameter `format` verwendet wird.

---

## Voraussetzungen

| Anforderung | Details |
|-------------|---------|
| **Authentifizierung** | Ein gültiges **JWT** (Bearer)-Token ist erforderlich. Holen Sie sich das Token über den im [Authentifizierungsleitfaden](/authentication/) beschriebenen **OAuth2**-Authentifizierungsflow. |
| **Speicher** | Die Arbeitsmappe muss sich in einem Aspose Cloud-Speicherort befinden. Liegt die Datei in einem Nicht-Standard-Speicher, geben Sie den Abfrageparameter `storageName` an. |
| **Ratenbegrenzung** | Die API folgt der standardmäßigen Aspose Cloud-Ratenbegrenzungsrichtlinie (Standard = 100 Anfragen/Minute pro Konto). |
| **SDKs (optional)** | Die Verwendung eines der offiziellen SDKs (C#, Java, Python, …) vereinfacht das Erstellen von Anfragen und die Verarbeitung von Antworten. Siehe den Abschnitt **SDK-Beispiele** weiter unten. |

---

## Anfrage

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Parameter | Typ | Ort | Erforderlich | Beschreibung |
|-----------|-----|------|-------------|-------------|
| **name** | `string` | Pfad | ✔️ | Name der Excel-Datei (einschließlich Erweiterung). |
| **sheetName** | `string` | Pfad | ✔️ | Arbeitsblatt, das das Listobjekt enthält. |
| **listobjectindex** | `integer` | Pfad | ✔️ | Nullbasierter Index des abzurufenden Listobjekts. |
| **format** | `string` | Abfrage | ❌ | Gewünschtes Exportformat (z. B. `pdf`, `csv`, `json`). |
| **folder** | `string` | Abfrage | ❌ | Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. |
| **storageName** | `string` | Abfrage | ❌ | Name des zu verwendenden Aspose Cloud-Speichers. |

#### Hinweise

* Alle Aufrufe **müssen** über HTTPS erfolgen.  
* Wenn der Parameter `format` angegeben ist, ist der Antworttext der exportierte Dateistream (z. B. `application/pdf`).  
* Ohne `format` gibt die API eine JSON-Beschreibung des ListObjects zurück.

---

## cURL-Beispiel

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*Ersetzen Sie `<your_jwt_token>` durch ein gültiges JWT, das Sie vom Authentifizierungsendpunkt erhalten haben.*

---

## Erfolgreiche Antwort (JSON)

Wenn **`format` weggelassen** wird, gibt die API eine JSON-Payload zurück, die das ListObject beschreibt.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

Wenn **`format` angegeben** ist, ist der Antworttext ein binärer Stream der angeforderten Dateityp (z. B. `Content-Type: text/csv`).

---

## Fehlerbehandlung

| HTTP-Code | Bedeutung | Beispiel-JSON |
|-----------|-----------|---------------|
| **400** | Ungültige Anfrage – fehlende oder ungültige Parameter. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | Nicht autorisiert – fehlendes oder ungültiges JWT-Token. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Listobjekt existiert nicht. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | Interner Serverfehler. | `{"Code":500,"Message":"Unexpected server error."}` |

### Häufige Fehlerquellen (Hinweise)

* **Nullbasierter Index** – `listobjectindex` beginnt bei **0**. Die Abfrage des Index `1` gibt die zweite Tabelle im Blatt zurück.  
* **Ordner & Speicher** – Wenn sich die Arbeitsmappe in einem Unterordner befindet, geben Sie den Abfrageparameter `folder` an (z. B. `?folder=Reports/2024`).  
* **Exportformat** – Nur vom Aspose.Cells-Konvertierungssystem unterstützte Formate sind zulässig (`pdf`, `xlsx`, `csv`, `json`, …). Die Angabe eines nicht unterstützten Werts führt zu einem **400**-Fehler.

---

## SDK-Beispiele

Die folgenden Codeausschnitte zeigen, wie der Endpunkt mithilfe der offiziellen Aspose.Cells Cloud SDKs aufgerufen wird. Ersetzen Sie Platzhalterwerte (`<YOUR_CLIENT>`, `<YOUR_JWT>` usw.) durch Ihre tatsächliche Konfiguration.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Initialisieren des API-Clients
var apiInstance = new ListObjectsApi();

// Anfrage erstellen
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // z. B. "csv" zum Exportieren
    folder: null,
    storageName: null
);

// Ausführen
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## Siehe auch

| Verwandter Endpunkt | Beschreibung |
|---------------------|-------------|
| **ListObject hinzufügen** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – neue Tabelle erstellen. |
| **ListObject aktualisieren** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – Tabelleneigenschaften ändern. |
| **ListObject löschen** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – Tabelle entfernen. |
| **Alle ListObjects auflisten** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – Tabellen in einem Arbeitsblatt auflisten. |

---

## Referenzen

* **OpenAPI-Spezifikation** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Authentifizierungsleitfaden** – <https://docs.aspose.cloud/cells/authentication/>  
* **GitHub-Repository (SDKs)** – <https://github.com/aspose-cells-cloud>  

---
---