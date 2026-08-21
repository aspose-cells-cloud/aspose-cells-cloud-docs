---
title: "Aspose.Cells Cloud API – Hämta listobjekt (tabell) från kalkylblad"
description: "Hämta ett ListObject (tabell) från ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Stöder export till flera format (PDF, CSV, JSON, …)."
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Tabell
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Hämta listobjekt (tabell) från kalkylblad

Hämta ett **listobjekt** (även kallat en *tabell*) från ett specifikt kalkylblad i en Excel-arbetsbok. Slutpunkten kan även exportera tabellen direkt till ett valt format genom att använda den valfria frågeparametern `format`.

---

## Förutsättningar

| Krav | Detaljer |
|------|----------|
| **Autentisering** | Ett giltigt **JWT**-token (Bearer) krävs. Skaffa token via **OAuth2**-autentiseringsflödet beskrivet i [Autentiseringsguide](/authentication/). |
| **Lagring** | Arbetsboken måste finnas i ett Aspose Cloud-lagringsområde. Om filen finns i en icke-standardlagring, ange `storageName`-frågeparametern. |
| **Hastighetsbegränsningar** | API:et följer Aspose Cloud:s standardhastighetsbegräsningspolicy (standard = 100 förfrågningar/minute per konto). |
| **SDK:er (valfritt)** | Användning av en av de officiella SDK:erna (C#, Java, Python, …) förenklar förfrågningskonstruktion och svarshantering. Se avsnittet **SDK-exempel** nedan. |

---

## Förfrågan

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Parameter | Typ | Plats | Obligatorisk | Beskrivning |
|-----------|-----|-------|--------------|-------------|
| **name** | `string` | Sökväg | ✔️ | Namn på Excel-filen (inklusive filtillägg). |
| **sheetName** | `string` | Sökväg | ✔️ | Kalkylbladet som innehåller listobjektet. |
| **listobjectindex** | `integer` | Sökväg | ✔️ | Nollbaserat index för listobjektet som ska hämtas. |
| **format** | `string` | Fråga | ❌ | Önskat exportformat (t.ex. `pdf`, `csv`, `json`). |
| **folder** | `string` | Fråga | ❌ | Mapp sökväg där arbetsboken lagras. |
| **storageName** | `string` | Fråga | ❌ | Namn på Aspose Cloud-lagring som ska användas. |

#### Anteckningar

* Alla anrop **måste** göras via HTTPS.  
* När `format`-parametern anges är svarsbrödtexten den exporterade filströmmen (t.ex. `application/pdf`).  
* Utan `format` returnerar API:et en JSON-beskrivning av ListObject.

---

## cURL-exempel

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*Ersätt `<your_jwt_token>` med ett giltigt JWT som erhållits från autentiseringsslutpunkten.*

---

## Lyckat svar (JSON)

När **`format` utelämnas** returnerar API:et en JSON-struktur som beskriver ListObject.

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

När **`format` anges** är svarsbrödtexten en binär ström i det begärda filformatet (t.ex. `Content-Type: text/csv`).

---

## Felhantering

| HTTP-kod | Betydelse | Exempel på JSON |
|----------|-----------|-----------------|
| **400** | Felaktig förfrågan – saknade eller ogiltiga parametrar. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | Auktorisering misslyckades – saknat eller ogiltigt JWT-token. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | Hittades inte – arbetsboken, kalkylbladet eller listobjektet finns inte. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | Internt serverfel. | `{"Code":500,"Message":"Unexpected server error."}` |

### Vanliga fallgropar (anteckningar)

* **Nollbaserat index** – `listobjectindex` börjar på **0**. En förfrågan till index `1` returnerar den andra tabellen i kalkylbladet.  
* **Mapp & lagring** – Om arbetsboken finns i en undermapp, inkludera `folder`-frågeparametern (t.ex. `?folder=Reports/2024`).  
* **Exportformat** – Endast format som stöds av Aspose.Cells konverteringsmotor tillåts (`pdf`, `xlsx`, `csv`, `json`, …). Ett ogiltigt värde orsakar ett **400**-fel.

---

## SDK-exempel

Följande kodsnuttar visar hur man anropar slutpunkten med de officiella Aspose.Cells Cloud SDK:erna. Ersätt plats hållar värden (`<YOUR_CLIENT>`, `<YOUR_JWT>` etc.) med din faktiska konfiguration.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Initiera API-klienten
var apiInstance = new ListObjectsApi();

// Bygg förfrågan
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // t.ex. "csv" för export
    folder: null,
    storageName: null
);

// Kör
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

## Se även

| Relaterad slutpunkt | Beskrivning |
|---------------------|-------------|
| **Lägg till ListObject** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – skapa en ny tabell. |
| **Uppdatera ListObject** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – ändra tabellens egenskaper. |
| **Ta bort ListObject** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – ta bort en tabell. |
| **Lista alla ListObjects** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – räkna upp tabeller i ett kalkylblad. |

---

## Referenser

* **OpenAPI-specifikation** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Autentiseringsguide** – <https://docs.aspose.cloud/cells/authentication/>  
* **GitHub-repo (SDK:er)** – <https://github.com/aspose-cells-cloud>  

---