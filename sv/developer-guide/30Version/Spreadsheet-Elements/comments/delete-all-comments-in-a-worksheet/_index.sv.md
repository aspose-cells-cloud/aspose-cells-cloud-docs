---
title: "Ta bort alla bladkommentarer"
description: "Ta bort alla kommentarer från ett kalkylblad i en Excel-fil med Aspose.Cells Cloud API:et. Lär dig DELETE-slutpunkten, nödvändiga parametrar, autentisering, exempel på cURL-begäran, svarsformat, felkoder och SDK-exempel."
keywords: "Aspose, Cells, ta bort kommentarer, kalkylblad, API, REST, Excel, moln"
url: /sv/comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Ta bort alla bladkommentarer

**API-version:** `v3.0`  
**Resurs:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud tillhandahåller en robust REST-slutpunkt som tar bort **alla** kommentarer från ett angivet kalkylblad. Denna åtgärd är oåterkallelig; när den har utförts kan kommentarerna inte återställas.

---

## Förutsättningar

| Krav | Detaljer |
|------|---------|
| **Autentisering** | Ett giltigt JWT-åtkomsttoken krävs i `Authorization`-headern (`Bearer <jwt token>`). Skaffa token via [OAuth2-autentiseringsflödet](https://docs.aspose.cloud/cells/authentication/). |
| **Lagring** | Filen måste finnas i en lagring som Aspose.Cells Cloud har tillgång till (standardlagring används om `storageName` utelämnas). |
| **Rättigheter** | Token måste ha behörighet att läsa och skriva målfilen. |
| **SDK:er (valfritt)** | SDK:er finns tillgängliga för .NET, Java, PHP, Ruby, Node.js, Python, Perl och Go (se avsnittet **SDK-exempel**). |

---

## HTTP-begäran

### Slutpunkt

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Sökvägsparametrar

| Namn        | Typ    | Beskrivning |
|-------------|--------|-------------|
| `name`      | string | Namn på Excel-filen (t.ex. `test.xlsx`). |
| `sheetName` | string | Namn på kalkylbladet (t.ex. `Sheet1`). |

### Frågeparametrar

| Namn          | Typ    | Obligatoriskt | Beskrivning |
|---------------|--------|---------------|-------------|
| `folder`      | string | valfritt      | Sökväg till mappen som innehåller filen. |
| `storageName` | string | valfritt      | Namn på den lagring där filen finns. |

### Begäranshuvuden

| Header            | Värde                              |
|-------------------|------------------------------------|
| `Authorization`   | `Bearer <jwt token>`               |
| `Accept`          | `application/json`                |
| `Content-Type`    | `application/json`                |

---

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Ersätt `test.xlsx`, `Sheet1`, `Documents`, `MyStorage` och `<jwt token>` med dina egna värden.*

---

## Svar

### Framgång (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Svarsbody följer modellen `CellsCloudResponse`.

### Felaktiga svar

| HTTP-kod | Betydelse                                 | Exempel på svarsbody |
|----------|-------------------------------------------|----------------------|
| **400**  | Felaktig begäran – ogiltiga parametrar.  | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**  | Inte auktoriserad – saknad/ogiltig JWT-token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**  | Ej hittad – fil eller kalkylblad finns inte. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**  | Internt serverfel.                        | `{ "Code": 500, "Message": "Server error." }` |

---

## SDK-exempel

Följande kodfragment visar hur slutpunkten anropas med de officiella Aspose.Cells Cloud SDK:erna (version 3.13.0). Ersätt platshållarvärden (`<fileName>`, `<sheet>`, `<jwt token>` etc.) med dina egna data.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | Filnamnet.
var sheetName = "Sheet1"; // string | Kalkylbladsnamnet.
var folder = "Documents"; // string | Mappsökväg (valfritt)
var storageName = "MyStorage"; // string | Lagringsnamn (valfritt)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComments: " + e.Message );
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
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
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
  puts "Exception when calling WorksheetsApi->delete_worksheet_comments: #{e}"
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
    .catch((error) => console.error("Error:", error));
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
    print("Exception when calling WorksheetsApi->delete_worksheet_comments:", e)
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
    print "Exception when calling WorksheetsApi->delete_worksheet_comments: $@\n";
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
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Anteckningar och begränsningar

* Denna åtgärd **tar bort alla kommentarer** i det angivna kalkylbladet. Använd den med försiktighet – det finns ingen ångra-funktion.
* Begäran **accepterar inte någon begäransbody**; all nödvändig information skickas via URL och headern.
* Om målfilen är **skyddad** eller om kalkylbladet är **skrivskyddat** returnerar API:et ett `400`- eller `401`-fel beroende på orsaken.
* Slutpunkten fungerar med filer som lagras i **Aspose Cloud Storage** samt med **Amazon S3**, **Azure Blob** eller **Google Cloud Storage** så länge de korrekt refereras via `storageName`.

---

## Relaterade resurser

* **OpenAPI-specifikation** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **Autentiseringsguide** – [OAuth2 för Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **SDK-repository** – <https://github.com/aspose-cells-cloud>
* **Allmän Worksheets API** – <https://docs.aspose.cloud/cells/worksheets/>

---

*Senast uppdaterad: 2026‑07‑30*