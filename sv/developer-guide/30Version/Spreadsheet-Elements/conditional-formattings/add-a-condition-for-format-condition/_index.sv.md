---
title: Lägg till villkor i villkorsformatering
description: Lär dig hur du lägger till ett villkor till en kalkylblads villkorsformatering med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, autentisering, cURL-exempel, SDK-utdrag och felhantering.
keywords: "Aspose.Cells Cloud, Villkorsformatering, Lägg till villkor, REST API, Excel, Kalkylblad"
type: docs
url: /conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# Lägg till villkor i villkorsformatering

Lägg till ett villkor i en befintlig villkorsformateringsregel i ett kalkylblad med Aspose.Cells Cloud REST API (v3.0).

---

## Förutsättningar

| Krav | Detaljer |
|------|----------|
| **Autentisering** | En giltig JWT-åtkomsttoken (Bearer) som erhålls via OAuth 2.0-flödet. |
| **API-version** | v3.0 – slutpunkts-URL:n innehåller `/v3.0/`. |
| **Lagring** | Arbetsboken måste finnas i ett lagringsutrymme som Aspose.Cells Cloud har tillgång till (standard är `Default`). |
| **Behörigheter** | Läs/skriv-behörighet för mål-arbetsboken. |
| **Stödda format** | Alla arbetsboksformat som stöds av Aspose.Cells (t.ex. `.xlsx`, `.xls`, `.xlsm`). |

---

## Slutpunkt

**HTTP-metod:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Parameter | Plats | Typ | Obligatorisk | Beskrivning |
|-----------|-------|-----|--------------|-------------|
| `name` | Sökväg | sträng | **Ja** | Namn på arbetsboksfilen (inklusive filtillägg). |
| `sheetName` | Sökväg | sträng | **Ja** | Namn på kalkylbladet som innehåller villkorsformateringen. |
| `index` | Sökväg | heltal | **Ja** | Nollbaserat index för villkorsformateringsamlingen som ska ändras. |
| `type` | Frågeparameter | sträng | **Ja** | Villkorstyp. Tillåtna värden: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Frågeparameter | sträng | **Ja** | Operator för villkoret. Tillåtna värden: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Frågeparameter | sträng | **Ja** | Första formeln/värdet kopplat till villkoret. |
| `formula2` | Frågeparameter | sträng | Nej | Andra formeln/värdet (obligatoriskt endast för operatorer som kräver två värden, t.ex. `Between`). |
| `folder` | Frågeparameter | sträng | Nej | Mapp i lagringen där arbetsboken finns. |
| `storageName` | Frågeparameter | sträng | Nej | Namn på lagringstjänsten. |

> **Obs:** Alla sökvägsparametrar (`name`, `sheetName`, `index`) och frågeparametrarna `type`, `operatorType`, `formula1` är obligatoriska. `formula2`, `folder` och `storageName` är valfria.

---

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*Ersätt `<jwt_token>` med en giltig åtkomsttoken och justera `name`, `sheetName`, `index` samt frågevärden enligt behov.*

---

## Lyckad svar

```json
{
  "Code": "200",
  "Status": "OK"
}
```

Svaret indikerar att villkoret lades framgångsrikt till. Åtgärden returnerar ett generiskt `CellsCloudResponse`-objekt som innehåller HTTP-statuskoden och ett kort statusmeddelande.

---

## Felaktiga svar

| HTTP-kod | Anledning | Exempel på kropp |
|----------|-----------|------------------|
| **400** | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Oauktoriserad – saknad eller ogiltig JWT-token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Ej hittad – arbetsbok, kalkylblad eller index för villkorsformatering finns inte. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | Internt serverfel – oväntat serverfel. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Anteckningar och vanliga fel

* **Parameterkodning** – URL-koda specialtecken i `formula1`/`formula2` (t.ex. mellanslag → `%20`).  
* **Operatorkompatibilitet** – Vissa operatorer (t.ex. `Between`) kräver både `formula1` och `formula2`. Utelämna `formula2` för operatorer som endast kräver ett enda värde.  
* **Index för villkorsformatering** – Indexet är nollbaserat. Använd **Get Conditional Formattings**-slutpunkten för att hämta rätt index om du är osäker.  
* **Lagringsmapp** – Om arbetsboken finns i en icke-standardmapp, ange frågeparametern `folder`; annars antar API:et rotmappen.  
* **Begränsning av förfrågningsfrekvens** – Aspose.Cells Cloud tillämpar begärandegränser per konto. Om du får ett 429-svar, vänta och försök igen efter en kort fördröjning.

---

## SDK-exempel

Här följer redo att köra-utdrag för de vanligaste SDK:erna. Ersätt platshållarvärden (`YOUR_FILE`, `YOUR_SHEET`, etc.) med dina egna data.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // valfritt
        string storageName = null;     // valfritt

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
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
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **Saknade SDK:er** – Om ett språk du behöver inte listas här, hänvisa till den allmänna **API-referensen** och skapa HTTP-begäran manuellt.

---

## Se även

- **[Hämta villkorsformateringar](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – Hämta listan över villkorsformateringsregler för ett kalkylblad.  
- **[Ta bort villkorsformatering](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – Ta bort en befintlig villkorsformateringsregel.  
- **[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – Helt maskinläsbar definition av denna åtgärd.  

---