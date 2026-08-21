---
title: "Beräkna alla formler i en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Beräkna"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, beräkna formler, Excel API, moln-SDK"
description: "Beräkna alla formler i en Excel-arbetsbok via Aspose.Cells Cloud REST API. Inkluderar cURL-exempel, begärparametrar, svarsschema, förutsättningar och SDK-fragment för flera språk."
weight: 140
ArticleTitle: "Beräkna alla formler i en Excel-arbetsbok"
---

Denna REST API beräknar **alla formler** i en Excel-arbetsbok.

**Förutsättningar:** Innan du anropar denna slutpunkt, se till att du har:
- En giltig JWT-autentiseringstoken. (Se [Autentiseringshandboken](/authentication/).)  
- Ditt Aspose.Cells Cloud-klient-ID och hemlighet.  
- Målarbetsboken har laddats upp till den angivna lagringsplatsen. (Se [Lagringsinställning](/storage/).)

## PostWorkbookCalculateFormula API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

Begärparametrarna listas nedan:

| Parameter Name  | Typ                | Plats  | Beskrivning                                                                           |
| --------------- | ------------------ | ------ | ------------------------------------------------------------------------------------- |
| **name**        | string             | path   | Namn på arbetsbokfilen.                                                               |
| **options**     | CalculationOptions | body   | JSON-objekt som anger beräkningsinställningar (t.ex. `CalcStackSize`, `IgnoreError`). |
| **ignoreError** | boolean            | query  | När `true` ignoreras fel som uppstår vid beräkning.                                   |
| **folder**      | string             | query  | Sökväg till mappen som innehåller arbetsboken.                                       |
| **storageName** | string             | query  | Namn på lagringstjänsten där arbetsboken lagras.                                      |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### Svarsdetaljer

| Fält             | Typ    | Beskrivning                                                             |
| ---------------- | ------ | ----------------------------------------------------------------------- |
| **Code**         | int    | HTTP-liknande statuskod (200 anger lyckat anrop).                      |
| **Status**       | string | Kort textuell beskrivning av resultatet (t.ex. `OK`).                  |
| **WorkbookUrl**  | string | Direkt URL där den uppdaterade arbetsboken kan laddas ned.             |
| **ErrorMessage** | string | Detaljerad felinformation vid misslyckad begäran; `null` vid lyckat anrop. |

#### Nästa steg / Vanliga fel

- **Hantera beräkningsfel** – ställ in `ignoreError=false` för att få ett felmeddelande när en formel inte kan utvärderas.
- **Hänseende till hastighetsbegränsning** – kontrollera `X-RateLimit-Remaining`-headern; om den når `0`, vänta innan du försöker igen.
- **Riktlinjer för HTTP-statuskoder**:
  - `400` – Ogiltiga begärparametrar.
  - `401` – Autentisering misslyckades (ogiltig eller utgången JWT).
  - `404` – Arbetsboken hittades inte.
  - `500` – Serverfel; kontakta Aspose-supporten om felet kvarstår.

| Kod | Betydelse             | När den returneras                                       |
|-----|-----------------------|----------------------------------------------------------|
| 400 | Felaktig begäran      | Ogiltiga begärparametrar eller felaktigt JSON-format.   |
| 401 | Auktorisering saknas  | Saknad, ogiltig eller utgången JWT-token.               |
| 404 | Hittades inte         | Angiven arbetsbok finns inte i lagringen.                |
| 500 | Internt serverfel     | Oväntat serverfel; kontakta Aspose-supporten.            |

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projekts uppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}