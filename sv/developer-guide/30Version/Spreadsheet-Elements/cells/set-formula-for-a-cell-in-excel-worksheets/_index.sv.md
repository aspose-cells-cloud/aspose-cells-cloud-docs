---
title: "Ställ in cellformel i Excel-arbetsblad"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, Ställ in formel, Arbetsblad, Cell, Molntjänst, cURL"
description: "Lär dig hur du ställer in en formel för en specifik cell i ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, fullständig parameterlista, felhantering och SDK-kodexempel."
---

Denna REST API ställer in en **cellformel** i en Excel-fil.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Förfrågningsparametrar**

| Parameter Name | Typ    | Plats  | Obligatorisk | Beskrivning                             |
|----------------|--------|--------|--------------|-----------------------------------------|
| name           | string | path   | Ja           | Namn på Excel-dokumentet.               |
| sheetName      | string | path   | Ja           | Namn på arbetsbladet.                   |
| cellName       | string | path   | Ja           | Adress till målcellen (t.ex. **A1**).   |
| value          | string | query  | Nej          | Värde att tilldela cellen.              |
| type           | string | query  | Nej          | Datatyp för värdet (t.ex. **string**).  |
| formula        | string | query  | Nej          | Formel som ska tillämpas på cellen (t.ex. **sum(A1,A2)**). |
| folder         | string | query  | Nej          | Mapp som innehåller dokumentet.         |
| storageName    | string | query  | Nej          | Namn på lagringstjänsten.               |

## **Svar**

Returnerar CellResponse.

- **Översikt över svarsfält**

| Fält            | Typ     | Beskrivning                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Adress till cellen (t.ex. `F341`).                    |
| `Row`           | integer | Radindex med nollbaserad indexering.                  |
| `Column`        | integer | Kolumnindex med nollbaserad indexering.               |
| `Value`         | string  | Cellens visade värde.                                 |
| `Type`          | string  | Cellens datatyp (t.ex. `IsString`).                   |
| `Formula`       | string  | Formeltext om cellen innehåller en formel.            |
| `IsFormula`     | bool    | Anger om cellen innehåller en formel.                 |
| `IsMerged`      | bool    | Anger om cellen är en del av ett sammanslagningsområde. |
| `IsArrayHeader` | bool    | Anger om cellen är en matrishuvudcell.                |
| `IsInArray`     | bool    | Anger om cellen tillhör en matris.                    |
| `IsErrorValue`  | bool    | Anger om cellen innehåller ett felvärde.              |
| `IsInTable`     | bool    | Anger om cellen finns i en tabell.                    |
| `IsStyleSet`    | bool    | Anger om en stil tillämpas på cellen.                 |
| `HtmlString`    | string  | HTML-kodad representation av cellens värde.           |
| `Style.link`    | object  | Hyperlänk till stilresursen.                          |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                        |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                   |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel.                                |

## Hur man använder PostWorksheetCellSetValue API med SDK:er

### PostWorksheetCellSetValue API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Använd verktyget cURL för att anropa Aspose.Cells-webbtjänster.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access-token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projekts uppgifter. Titta i [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C#-exempel – ställ in formel för en cell
// Ersätt <access-token>, <file-name> etc. med dina värden.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java-exempel – ställ in formel för en cell
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP-exempel – ställ in formel för en cell
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby-exempel – ställ in formel för en cell
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python-exempel – ställ in formel för en cell
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js-exempel – ställ in formel för en cell
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java)-exempel – ställ in formel för en cell
// Liknande standard-Java-exemplet; se till att använda den Android-kompatibla SDK:en.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Swift-exempel finns inte tillgängligt**. SDK för Swift är för närvarande under utveckling.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl-exempel – ställ in formel för en cell
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go-exempel – ställ in formel för en cell
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}