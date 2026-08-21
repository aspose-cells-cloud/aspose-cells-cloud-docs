---
title: "Delete Worksheet Comment API – Aspose.Cells Cloud"
description: "Löschen Sie einen bestimmten Zellkommentar in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält Endpunkt, Parameter, Beispielanfragen/-antworten, SDK-Ausschnitte und Fehlerbehandlung."
keywords: "Aspose.Cells, Kommentar löschen, Excel-API, REST, Arbeitsblatt-Kommentar"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# Delete Worksheet Comment API – Aspose.Cells Cloud

> **Seite zuletzt aktualisiert:** 30. Juli 2026  

## Übersicht
Ein **Kommentar** ist eine Textnotiz, die einer bestimmten Zelle in einem Excel-Arbeitsblatt zugeordnet ist.  
Die Operation **Delete Worksheet Comment** (Arbeitsblatt-Kommentar löschen) entfernt den Kommentar aus der angegebenen Zelle.

![Aspose.Cells Cloud – Illustration zum Löschen von Arbeitsblatt-Kommentaren](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – Delete Worksheet Comment API")

## Authentifizierung
Alle Aspose.Cells Cloud-Endpunkte erfordern eine **JWT-Token-basierte Authentifizierung**.  
Geben Sie das Token im `Authorization`-Header an:

```
Authorization: Bearer <jwt token>
```

Einzelheiten zum Abrufen eines JWT-Tokens finden Sie im [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Voraussetzungen
- Ein gültiges JWT-Zugriffstoken.  
- Die Zielarbeitsmappe (`{name}`) muss sich am angegebenen Speicherort befinden.  
- Optional: Eines der Aspose.Cells Cloud SDKs für Ihre bevorzugte Programmiersprache ist installiert.

## HTTP-Anfrage

### Endpunkt
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Pfadparameter
| Parameter | Typ    | Erforderlich | Beschreibung |
|-----------|--------|--------------|-------------|
| `name`      | string | ✅ | Der Name der Excel-Arbeitsmappe (z. B. `test.xlsx`). |
| `sheetName` | string | ✅ | Der Name des Arbeitsblatts, das den Kommentar enthält. |
| `cellName`  | string | ✅ | Die Adresse der Zelle, deren Kommentar gelöscht werden soll (z. B. `A1`). |

### Abfrageparameter
| Parameter   | Typ    | Erforderlich | Beschreibung |
|-------------|--------|--------------|-------------|
| `folder`      | string | ❌ | Pfad zum Ordner, in dem die Arbeitsmappe gespeichert ist. Falls weggelassen, wird der Root-Ordner verwendet. |
| `storageName` | string | ❌ | Name des Speicherdiensts (z. B. `MyCloud`). Falls weggelassen, wird der Standardspeicher verwendet. |

## Beispielanfrage

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Antwort

### Erfolg (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |
### Fehlerantworten

| HTTP-Code | Beschreibung | Beispiel |
|-----------|-------------|---------|
| 400 | Bad request – fehlende oder fehlerhafte Parameter. | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | Unauthorized – ungültiges oder fehlendes Token. | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | Not found – Datei, Arbeitsblatt oder Kommentar existiert nicht. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | Internal server error – unerwarteter Zustand auf dem Server. | `{ "Code": 500, "Message": "Server error." }` |

## SDK-Beispiele
Im Folgenden finden Sie sofort ausführbare Codeausschnitte für die gängigsten Sprachen. Ersetzen Sie `<jwt token>`, `test.xlsx`, `Sheet1` und `A1` durch Ihre eigenen Werte.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Konfigurieren des API-Clients
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Kommentar gelöscht. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Ausnahme beim Aufruf von WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Kommentar gelöscht, Status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Ausnahme beim Aufruf von WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Kommentar gelöscht. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Ausnahme beim Aufruf von WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Kommentar gelöscht – Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Ausnahme beim Aufruf von WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Kommentar gelöscht. Status:", response.status);
    })
    .catch((error) => {
        console.error("Fehler beim Löschen des Kommentars:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Kommentar gelöscht. Status:", response.status)
except Exception as e:
    print("Ausnahme beim Aufruf von WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Kommentar gelöscht. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Ausnahme beim Aufruf von WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (optional)
        "MyStorage",   // storageName (optional)
    )
    if err != nil {
        fmt.Printf("Fehler beim Aufruf von DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Kommentar gelöscht. Status: %s\n", result.Status)
}
```

## Verwandte Vorgänge
- [Add Worksheet Comment](/comments/add/)  
- [Update Worksheet Comment](/comments/update/)  

## Ratenbegrenzung
Aspose.Cells Cloud erzwingt standardmäßig eine **Ratenbegrenzung von 100 Anfragen pro Minute pro Konto**. Das Überschreiten dieses Limits führt zu HTTP 429 Too Many Requests. Implementieren Sie exponentielles Backoff oder beachten Sie den Header `Retry-After`, um Throttling zu vermeiden.

## Siehe auch
- **OpenAPI-Spezifikation:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Authentifizierungsleitfaden:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **SDK-Repository:** <https://github.com/aspose-cells-cloud>  

---