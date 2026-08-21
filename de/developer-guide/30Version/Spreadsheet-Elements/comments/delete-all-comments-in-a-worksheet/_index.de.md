---
title: "Alle Arbeitsblatt-Kommentare löschen"
description: "Löschen Sie alle Kommentare aus einem Arbeitsblatt in einer Excel-Datei mithilfe der Aspose.Cells Cloud API. Erfahren Sie mehr über den DELETE-Endpunkt, erforderliche Parameter, Authentifizierung, Beispiel-cURL-Anforderung, Antwortformat, Fehlercodes und SDK-Beispiele."
keywords: "Aspose, Cells, Kommentare löschen, Arbeitsblatt, API, REST, Excel, Cloud"
url: /de/comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Alle Arbeitsblatt-Kommentare löschen

**API-Version:** `v3.0`  
**Ressource:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud bietet einen robusten REST-Endpunkt, der **alle** Kommentare aus einem angegebenen Arbeitsblatt entfernt. Dieser Vorgang ist unwiderruflich; sobald er ausgeführt wurde, können die Kommentare nicht wiederhergestellt werden.

---

## Voraussetzungen

| Anforderung | Details |
|-------------|---------|
| **Authentifizierung** | Ein gültiges JWT-Zugriffstoken ist im `Authorization`-Header erforderlich (`Bearer <jwt token>`). Holen Sie sich das Token über den [OAuth2-Authentifizierungsfluss](https://docs.aspose.cloud/cells/authentication/). |
| **Speicher** | Die Datei muss sich in einem Speicher befinden, der für Aspose.Cells Cloud zugänglich ist (Standard-Speicher wird verwendet, wenn `storageName` weggelassen wird). |
| **Berechtigungen** | Das Token muss über die Berechtigung zum Lesen und Schreiben der Ziel-Datei verfügen. |
| **SDKs (optional)** | SDKs sind für .NET, Java, PHP, Ruby, Node.js, Python, Perl und Go verfügbar (siehe Abschnitt **SDK-Beispiele**). |

---

## HTTP-Anforderung

### Endpunkt

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Pfad-Parameter

| Name        | Typ    | Beschreibung |
|-------------|--------|--------------|
| `name`      | string | Name der Excel-Datei (z. B. `test.xlsx`). |
| `sheetName` | string | Name des Arbeitsblatts (z. B. `Sheet1`). |

### Abfrage-Parameter

| Name            | Typ    | Erforderlich | Beschreibung |
|-----------------|--------|--------------|--------------|
| `folder`        | string | optional     | Pfad zum Ordner, der die Datei enthält. |
| `storageName`   | string | optional     | Name des Speichers, in dem sich die Datei befindet. |

### Anforderungs-Header

| Header                | Wert                               |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer <jwt token>`               |
| `Accept`              | `application/json`                |
| `Content-Type`        | `application/json`                |

---

## Beispielanforderung (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Ersetzen Sie `test.xlsx`, `Sheet1`, `Documents`, `MyStorage` und `<jwt token>` durch Ihre tatsächlichen Werte.*

---

## Antwort

### Erfolg (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Der Antwort-Text entspricht dem Modell `CellsCloudResponse`.

### Fehlerantworten

| HTTP-Code | Bedeutung                              | Beispiel-Antworttext |
|-----------|----------------------------------------|----------------------|
| **400**   | Ungültige Anforderung – ungültige Parameter. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**   | Nicht authentifiziert – fehlendes/ungültiges JWT-Token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Nicht gefunden – Datei oder Arbeitsblatt existiert nicht. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**   | Interner Serverfehler. | `{ "Code": 500, "Message": "Server error." }` |

---

## SDK-Beispiele

Die folgenden Codeausschnitte zeigen, wie der Endpunkt mit den offiziellen Aspose.Cells Cloud SDKs (Version 3.13.0) aufgerufen wird. Ersetzen Sie Platzhalterwerte (`<fileName>`, `<sheet>`, `<jwt token>` usw.) durch Ihre eigenen Daten.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | Der Dateiname.
var sheetName = "Sheet1"; // string | Der Name des Arbeitsblatts.
var folder = "Documents"; // string | Ordnerpfad (optional)
var storageName = "MyStorage"; // string | Speichername (optional)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Ausnahme beim Aufruf von WorksheetsApi.DeleteWorksheetComments: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Ausnahme beim Aufruf von WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # optional
storage_name = 'MyStorage'    # optional

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Ausnahme beim Aufruf von WorksheetsApi->delete_worksheet_comments: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Fehler:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # optional
storage_name = "MyStorage"    # optional

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Ausnahme beim Aufruf von WorksheetsApi->delete_worksheet_comments:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Ausnahme beim Aufruf von WorksheetsApi->delete_worksheet_comments: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Fehler: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Hinweise & Einschränkungen

* Dieser Vorgang **löscht alle Kommentare** im angegebenen Arbeitsblatt. Nutzen Sie ihn mit Vorsicht – es gibt keine Rückgängig-Funktion.
* Die Anforderung **akzeptiert keinen Anforderungstext**; alle erforderlichen Informationen werden über die URL und Header übermittelt.
* Wenn die Ziel-Datei **geschützt** ist oder das Arbeitsblatt **schreibgeschützt** ist, gibt die API je nach zugrunde liegender Ursache einen Fehler `400` oder `401` zurück.
* Der Endpunkt funktioniert mit Dateien, die in **Aspose Cloud Storage** gespeichert sind, ebenso wie mit **Amazon S3**, **Azure Blob** oder **Google Cloud Storage**, sofern diese korrekt über `storageName` referenziert werden.

---

## Verwandte Ressourcen

* **OpenAPI-Spezifikation** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **Authentifizierungsanleitung** – [OAuth2 für Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **SDK-Repository** – <https://github.com/aspose-cells-cloud>
* **Allgemeine Worksheets API** – <https://docs.aspose.cloud/cells/worksheets/>

---

*Zuletzt aktualisiert: 2026‑07‑30*