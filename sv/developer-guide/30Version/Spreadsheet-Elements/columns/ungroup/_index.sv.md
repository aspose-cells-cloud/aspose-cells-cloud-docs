---
title: Gruppera bort kolumner i Excel – Aspose.Cells Cloud API  
description: Ta bort kolumngrouping i ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, autentisering, cURL-exempel, svarsformat och SDK-utdrag.  
keywords: Aspose.Cells, avgruppera, kolumner, Excel, API, REST, moln, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Gruppera bort kolumner i Excel  

Aspose.Cells Cloud tillhandahåller en **POST**-åtgärd som tar bort kolumngrouping från ett angivet kalkylark. Den här sidan beskriver begärandeformatet, nödvändiga parametrar, autentiseringsmetod, exempel på anrop och SDK-användning.  

---  

## Förutsättningar  

| Krav | Varför det behövs |
|------|-----------------|
| **Aspose Cloud-konto** | Åtkomst till Aspose.Cells Cloud-tjänsterna. |
| **JWT-åtkomsttoken** | Alla API-anrop måste auktoriseras med en bearer-token. Se [JWT-autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Arbetsbok lagrad i Aspose Cloud-lagring** | API:t fungerar på filer som finns i molnlagringen (eller en ansluten extern lagring). |
| **Kalkylarksnamn** | Målkalkylarket måste finnas i arbetsboken. |

---  

## Autentisering  

Alla begäranden kräver ett **Authorization**-huvud som innehåller en giltig JWT-token:  

```http
Authorization: Bearer <access_token>
```  

Token erhålls via Aspose Cloud OAuth-flödet. Tokens är giltiga under en begränsad tid; uppdatera vid behov.  

---  

## Slutpunkt  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```  

* `{name}` – **Sökväg** – Arbetsboksfilens namn (t.ex. `test.xlsx`).  
* `{sheetName}` – **Sökväg** – Kalkylarksnamn (t.ex. `Sheet1`).  

---  

## Parametrar  

### Sökvägsparametrar  

| Namn | Typ | Nödvändig | Beskrivning |
|------|-----|-----------|-------------|
| `name` | sträng | Ja | Arbetsboksfilens namn. |
| `sheetName` | sträng | Ja | Kalkylarksnamnet. |

### Frågeparametrar  

| Namn | Typ | Nödvändig | Beskrivning |
|------|-----|-----------|-------------|
| `firstIndex` | heltal | Ja | Nollbaserat index för den första kolumnen som ska avgrupperas. |
| `lastIndex` | heltal | Ja | Nollbaserat index för den sista kolumnen som ska avgrupperas. |
| `folder` | sträng | Nej | Sökväg till mappen som innehåller arbetsboken. |
| `storageName` | sträng | Nej | Namn på lagringstjänsten där filen finns. |

---  

## Exempel på begäran (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```  

*Ersätt `<access_token>` med en giltig JWT-token.*  

---  

## Lyckad svarsrespons  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```  

Svarsobjektet (`CellsCloudResponse`) innehåller intervallet av kolumner som framgångsrikt avgrupperades.  

### Felrespons  

När begäran misslyckas returnerar tjänsten en JSON-payload med följande fält:  

| Fält | Betydelse |
|------|-----------|
| `Code` | HTTP-liknande felkod (t.ex. 400, 401). |
| `Status` | Kort beskrivning av felet. |
| `ErrorMessage` | Detaljerad felbeskrivning. |

---  

**HTTP-statuskoder**  

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast | Uppladdad fil överskrider storleksgränsen. |
| 500 | Internt serverfel | Oväntat serverfel. |
---  

## SDK-utdrag  

Nedan finns redo att köra kodexempel för de mest populära SDK:erna. Ersätt platshållarvärden (`<YourAccessToken>`, `<YourFileName>` etc.) med egna uppgifter.  

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **Obs:** SDK:er för PHP, Ruby, Perl och andra språk följer samma parameterordning. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för fullständiga exempel.  

---  

## Referenser  

* **OpenAPI-specifikation:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Autentiseringsguide:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **SDK-lager:** <https://github.com/aspose-cells-cloud>  

---  

## Versionshistorik  

| Datum | Författare | Ändring |
|-------|------------|---------|
| 2026‑07‑30 | AI Optimizer | Åtgärdade UTF‑8-kodning, lade till Förutsättningar, rensade metanyckelord, förbättrade rubrikhierarki och infogade SDK-utdrag. |
| 2026‑07‑29 | Original | Första utkast till dokumentation. |

---