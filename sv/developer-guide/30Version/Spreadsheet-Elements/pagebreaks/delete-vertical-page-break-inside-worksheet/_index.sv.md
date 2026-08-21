---
title: Ta bort vertikalt sidbrytning – Aspose.Cells Cloud REST API
description: Ta bort ett vertikalt sidbrytning från ett Excel-ark med hjälp av Aspose.Cells Cloud REST API (v3.0). Inkluderar begärsyntax, parametrar, exempel, svarskoder och SDK-utdrag.
keywords: ta bort vertikalt sidbrytning, Aspose.Cells Cloud, REST API
slug: ta-bort-vertikalt-sidbrytning
api_version: v3.0
---

# Ta bort vertikalt sidbrytning

Ta bort ett vertikalt sidbrytning från ett ark i en Excel-fil med hjälp av Aspose.Cells Cloud REST API.

---

## Förutsättningar

* Ett **JWT-autentiseringstoken** måste anges i `Authorization`-headern.  
* Arbetsboken (`{name}`) måste finnas i den angivna **mappen** eller **lagringen** och vara tillgänglig för API-klienten.

---

## HTTP-begäran

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Parameter   | Typ     | Plats  | Obligatorisk | Beskrivning |
|-------------|---------|--------|--------------|-------------|
| **name**      | string | path   | Ja           | Namnet på Excel-filen. |
| **sheetName** | string | path   | Ja           | Namnet på det ark som innehåller sidbrytningen. |
| **index**     | integer| path   | Ja           | Nollbaserat index för det vertikala sidbrytningen som ska tas bort. |
| **folder**    | string | query  | Nej          | Mappväg där filen är lagrad. |
| **storageName**| string| query  | Nej          | Namn på lagringstjänsten. |

---

## Exempel på begäran

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Lyckad svars Kod

| Kod  | Beskrivning |
|------|-------------|
| **200** | Det vertikala sidbrytningen togs framgångsrikt bort. |

**Exempel på nyttolast**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Felaktiga svar

| HTTP-kod | Beskrivning |
|----------|-------------|
| **401** | Otillåten – saknat eller ogiltigt token. |
| **404** | Ej hittad – den angivna filen, arbetsbladet eller sidbrytningsindexet finns inte. |
| **400** | Felaktig begäran – felaktig begärsyntax eller ogiltiga parametrar. |
| **500** | Internt serverfel – ett oväntat tillstånd upptäcktes. |

**Exempel på felaktiga nyttolaster**

*401 – Otillåten*

```json
{
  "Code": 401,
  "Message": "Ogiltigt autentiseringstoken."
}
```

*404 – Ej hittad*

```json
{
  "Code": 404,
  "Message": "Den angivna filen, arbetsbladet eller sidbrytningsindexet hittades inte."
}
```

*400 – Felaktig begäran*

```json
{
  "Code": 400,
  "Message": "Begärans parametrar är ogiltiga eller felaktigt formaterade."
}
```

*500 – Internt serverfel*

```json
{
  "Code": 500,
  "Message": "Ett oväntat serverfel uppstod."
}
```

---

## SDK-exempel

Följande exempel visar hur **DeleteVerticalPageBreak**-operationen anropas med olika Aspose.Cells Cloud SDK:n.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(SDK-utdrag för PHP, Ruby, Perl och andra språk följer samma mönster och finns tillgängliga i det officiella GitHub-arkivet.)*

---

## Relaterade resurser

* **OpenAPI-specifikation** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **Aspose.Cells Cloud SDK:n** – <https://github.com/aspose-cells-cloud>  
* **Autentiseringsguide** – <https://docs.aspose.cloud/cells/authentication/>  

---

*Dokumentet senast uppdaterat: 2026‑07‑30*