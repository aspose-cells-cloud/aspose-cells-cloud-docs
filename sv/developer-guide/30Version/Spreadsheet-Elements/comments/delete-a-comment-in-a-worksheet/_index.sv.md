---
---
title: "Ta bort arbetsbladkommentar-API – Aspose.Cells Cloud"
description: "Ta bort en specifik cellkommentar i ett Excel-arbetsblad med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, exempel på begäran/svar, SDK-utdrag och felhantering."
keywords: "Aspose.Cells, ta bort kommentar, Excel-API, REST, arbetsbladkommentar"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# Ta bort arbetsbladkommentar-API – Aspose.Cells Cloud

> **Senast uppdaterad sida:** 30 juli 2026  

## Översikt
En **kommentar** är en textanteckning kopplad till en viss cell i ett Excel-arbetsblad.  
Operationen **Ta bort arbetsbladkommentar** tar bort en kommentar från den angivna cellen.

![Aspose.Cells Cloud – Illustration för ta bort arbetsbladkommentar](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – API för ta bort arbetsbladkommentar")

## Autentisering
Alla Aspose.Cells Cloud-slutpunkter kräver **JWT-tokenbaserad autentisering**.  
Inkludera token i `Authorization`-headern:

```
Authorization: Bearer <jwt token>
```

För detaljer om hur du erhåller en JWT-token, se [Autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Förutsättningar
- En giltig JWT-åtkomsttoken.  
- Den målmappbok (`{name}`) måste finnas på den angivna lagringsplatsen.  
- Valfritt: Ett av Aspose.Cells Cloud SDK:n installerat för din föredragna programmeringsspråk.

## HTTP-begäran

### Slutpunkt
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Sökvägsparametrar
| Parameter | Typ   | Krävs | Beskrivning |
|-----------|-------|-------|-------------|
| `name`      | sträng | ✅ | Namnet på Excel-mappboken (t.ex. `test.xlsx`). |
| `sheetName` | sträng | ✅ | Namnet på arbetsbladet som innehåller kommentaren. |
| `cellName`  | sträng | ✅ | Adressen till den cell vars kommentar ska tas bort (t.ex. `A1`). |

### Frågeparametrar
| Parameter   | Typ   | Krävs | Beskrivning |
|-------------|-------|-------|-------------|
| `folder`      | sträng | ❌ | Sökväg till mappen där mappboken lagras. Om utelämnas används rotmappen. |
| `storageName` | sträng | ❌ | Namnet på lagringstjänsten (t.ex. `MyCloud`). Om utelämnas används standardlagring. |

## Exempel på begäran

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Svar

### Lyckades (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                     | Beskrivning                                      |
|-----|-------------------------------|--------------------------------------------------|
| 200 | OK                            | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran              | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast            | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel             | Oväntat serverfel. |
### Felaktiga svar

| HTTP-kod | Beskrivning | Exempel |
|----------|-------------|---------|
| 400 | Felaktig begäran – saknade eller felaktiga parametrar. | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | Autentisering krävs – ogiltig eller saknad token. | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | Ej hittad – filen, arbetsbladet eller kommentaren finns inte. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | Internt serverfel – oväntat tillstånd på servern. | `{ "Code": 500, "Message": "Server error." }` |

## SDK-exempel
Nedan finns redo-användbara kodstycken för de mest populära språken. Ersätt `<jwt token>`, `test.xlsx`, `Sheet1` och `A1` med dina egna värden.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Konfigurera API-klienten
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
    Console.WriteLine("Kommentar borttagen. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Undantag vid anrop av WorksheetsApi.DeleteWorksheetComment: " + e.Message);
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
            System.out.println("Kommentar borttagen, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Undantag vid anrop av WorksheetsApi#deleteWorksheetComment");
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
    echo "Kommentar borttagen. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Undantag vid anrop av WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
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
  puts "Kommentar borttagen – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Undantag vid anrop av WorksheetsApi->delete_worksheet_comment: #{e}"
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
        console.log("Kommentar borttagen. Status:", response.status);
    })
    .catch((error) => {
        console.error("Fel vid borttagning av kommentar:", error);
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
    print("Kommentar borttagen. Status:", response.status)
except Exception as e:
    print("Undantag vid anrop av WorksheetsApi->delete_worksheet_comment:", e)
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
    print "Kommentar borttagen. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Undantag vid anrop av WorksheetsApi->delete_worksheet_comment: $@\n";
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
        "Docs",        // folder (valfritt)
        "MyStorage",   // storageName (valfritt)
    )
    if err != nil {
        fmt.Printf("Fel vid anrop av DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Kommentar borttagen. Status: %s\n", result.Status)
}
```

## Relaterade operationer
- [Lägg till arbetsbladkommentar](/comments/add/)  
- [Uppdatera arbetsbladkommentar](/comments/update/)  

## Rate limiting
Aspose.Cells Cloud har en standard **hastighetsbegränsning på 100 begäranden per minut per konto**. Överskridning av denna gräns returnerar HTTP 429 Too Many Requests. Implementera exponentiell backoff eller respektera `Retry-After`-headern för att undvika throttling.

## Se även
- **OpenAPI-specifikation:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Autentiseringsguide:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **SDK-repository:** <https://github.com/aspose-cells-cloud>  

---