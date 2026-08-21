---
title: Lägg till CellArea i villkorsformatering
description: Lägg till ett cellområde i en villkorsformateringsregel i ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, cURL- och SDK-exempel, svarschema och felhantering.
keywords: Aspose.Cells, Villkorsformatering, CellArea, REST API, Excel, moln-SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Lägg till CellArea i villkorsformatering

**Sammanfattning** – Lägger till ett cellområde till en befintlig villkorsformateringsregel i ett ark.

---

## Förutsättningar

1. **Aspose.Cells Cloud-konto** – skaffa din **App SID** och **App Key**.  
2. **JWT-token** – generera en JWT-token med App SID/Key (se [autentiseringshandboken](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. Målexcelfilen måste redan finnas i den angivna lagringen/mappen.

---

## Autentisering

Alla anrop kräver **JWT-tokenbaserad autentisering**. Skicka token i `Authorization`-headern:

```http
Authorization: Bearer <jwt token>
```

---

## HTTP-begäran

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Sökvägsparametrar

| Namn        | Typ    | Beskrivning                                  |
|-------------|--------|----------------------------------------------|
| `name`      | string | Excelfilens namn (t.ex. `Book1.xlsx`).      |
| `sheetName` | string | Arket som innehåller regeln (t.ex. `Sheet1`). |
| `index`     | integer| Nollbaserat index för villkorsformateringsregeln. |

### Frågeparametrar

| Namn          | Typ    | Obligatoriskt | Beskrivning                                      |
|---------------|--------|---------------|--------------------------------------------------|
| `cellArea`    | string | **Ja**        | Cellområde att lägga till, i A1-notation (t.ex. `A1:C3`). |
| `folder`      | string | Nej           | Mappsökväg där filen lagras.                    |
| `storageName` | string | Nej           | Namn på lagringstjänsten.                       |

---

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Förväntat lyckat svar

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Svarschema – `CellArea`**

| Egenskap       | Typ | Beskrivning                              |
|----------------|-----|------------------------------------------|
| `StartRow`     | int | Nollbaserat index för första raden.      |
| `StartColumn`  | int | Nollbaserat index för första kolumnen.   |
| `EndRow`       | int | Nollbaserat index för sista raden.       |
| `EndColumn`    | int | Nollbaserat index för sista kolumnen.    |

---

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                      |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.    |
| 500 | Internal Server Error       | Oväntat serverfel.                                    |
---

## SDK-exempel

Nedan finns korta kodsnuttar för de vanligaste SDK:erna. Ersätt `YOUR_APP_SID` och `YOUR_APP_KEY` med dina inloggningsuppgifter, och ange den genererade JWT-token dit det krävs.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Anteckningar & tips

- **CellArea-format** – Måste vara ett giltigt A1-område (`A1`, `A1:C3`, `Sheet2!B2:D5`). Ogiltiga format returnerar **400 Bad Request**.
- **Överlappande områden** – Att lägga till ett område som överlappar ett befintligt område i samma regel orsakar **409 Conflict**.
- **Nollbaserad indexering** – Rad- och kolumnindex i svaret börjar på `0`. Konvertera till Excels 1-baserade notation om nödvändigt.
- **Lagring** – Om du utelämnar `folder` och `storageName` använder API:t standardlagringen/root-mappen.

---

## Relaterade åtgärder

- **Ta bort CellArea** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Lägg till villkor i villkorsformatering** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Hämta villkorsformatering** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

Dessa åtgärder kan kombineras för att bygga fullständiga villkorsformateringsarbetsflöden.

---
---