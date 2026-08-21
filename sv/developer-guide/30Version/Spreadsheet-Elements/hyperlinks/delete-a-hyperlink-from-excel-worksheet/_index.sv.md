---
title: "Ta bort hyperlänk i kalkylblad"
type: docs
url: /sv/hyperlinks/delete/
description: "Ta bort en hyperlänk i kalkylblad med hjälp av index via Aspose.Cells Cloud API. Lär dig vilka parametrar som krävs, hur autentisering fungerar, och se kodexempel för C#, Java, Python och mer."
keywords: "Aspose.Cells, moln, ta bort hyperlänk, Excel API, REST, hyperlänk i kalkylblad"
ArticleTitle: "Ta bort hyperlänk i kalkylblad – Aspose.Cells Cloud API-dokumentation"
weight: 40
---

Denna REST API tar bort en hyperlänk i kalkylblad baserat på dess index i ett Excel-kalkylblad.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Parametrar för begäran

| Parameternamn      | Typ     | Plats  | Obligatorisk | Beskrivning                                                       |
| ------------------ | ------- | ------ | ------------ | ----------------------------------------------------------------- |
| **name**           | string  | path   | ✅           | Namn på Excel-dokumentet.                                         |
| **sheetName**      | string  | path   | ✅           | Namn på kalkylbladet.                                             |
| **hyperlinkIndex** | integer | path   | ✅           | Nollbaserat index för den hyperlänk som ska tas bort.             |
| **folder**         | string  | query  | ❌           | Mapp som innehåller dokumentet (standard: rotmapp).               |
| **storageName**    | string  | query  | ❌           | Namn på lagringstjänsten (standardlagring används om utelämnas). |

#### Svar

| Statuskod                     | Beskrivning                                              | Exempel på responsbody                              |
| ----------------------------- | -------------------------------------------------------- | --------------------------------------------------- |
| **200 OK**                    | Hyprlänken har tagits bort utan problem.                | `{"Code":200,"Status":"OK"}`                        |
| **400 Bad Request**           | Saknade eller ogiltiga parametrar.                       | `{"Code":400,"Message":"Ogiltigt hyperlinkIndex."}` |
| **401 Unauthorized**          | Autentiseringstoken saknas eller är ogiltig.             | `{"Code":401,"Message":"Ogiltig åtkomsttoken."}`    |
| **404 Not Found**             | Filen, kalkylbladet eller hyperlänkindexet finns inte. | `{"Code":404,"Message":"Resursen hittades inte."}`  |
| **500 Internal Server Error** | Oväntat serverfel.                                       | `{"Code":500,"Message":"Internt serverfel."}`       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Exempel nedan visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er. Inline-kodstycken tillhandahålls för pålitlighet; en länk till den ursprungliga Gist-behålls för referens.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Källa: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Källa: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Källa: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
// Källa: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Källa: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Hyperlänk borttagen"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
// Källa: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlänk borttagen')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
// Källa: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Källa: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hyperlänk borttagen")
    }
}
```

{{< /tab >}}

{{< /tabs >}}