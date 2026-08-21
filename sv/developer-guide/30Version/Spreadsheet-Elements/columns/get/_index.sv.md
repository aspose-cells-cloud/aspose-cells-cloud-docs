---
title: Hämta kolumninformation – Aspose.Cells Cloud API-referens (v4.0)
description: hämta detaljerad information om en kolumn i ett kalkylblad (index, bredd, stil, dolt tillstånd) med Aspose.Cells Cloud REST API.
keywords: Aspose.Cells, moln-API, Excel-kolumn, hämta kolumn, REST API, JWT, kalkylblad
date: 2026-07-30
---

# Hämta kolumninformation

Hämta detaljerad information om en specifik kolumn i ett kalkylblad (index, bredd, stil, dolt tillstånd) från en Excel-arbetsbok som lagras i Aspose Cloud.

## Innehållsförteckning

1. [Förutsättningar](#prerequisites)
2. [Autentisering](#authentication)
3. [Slutpunkt](#endpoint)
4. [Begäransparametrar](#request-parameters)
5. [cURL-exempel](#curl-example)
6. [Svarsexempel](#response-example)
7. [Svarschema](#response-schema)
8. [ Möjliga fel](#possible-errors)
9. [SDK-exempel](#sdk-examples)
10. [Ytterligare resurser](#additional-resources)

---

## Förutsättningar

- En giltig **JWT-åtkomsttoken** som erhållits via Aspose Cloud-autentisering.
- Arbetsboksfilen måste vara lagrad i Aspose Cloud Storage (eller ett annat stöddat lagringsutrymme), och mappbanen (om någon finns) måste vara känd.

---

## Autentisering

Alla Aspose.Cells Cloud-API:n använda **JWT-tokenbaserad autentisering**. Inkludera token i `Authorization`-headern:

```http
Authorization: Bearer <access_token>
```

För detaljerad information om hur du erhåller en token, se [autentiseringsguiden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Slutpunkt

```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – arbetsbokens filnamn (t.ex. `test.xlsx`).
- **{sheetName}** – kalkylbladets namn (t.ex. `Sheet1`).
- **{columnIndex}** – nollbaserat index för kolumnen som ska hämtas.

---

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## Begäransparametrar

| Namn            | Plats | Typ     | Obligatorisk | Beskrivning                                              |
| --------------- | ----- | ------- | ------------ | -------------------------------------------------------- |
| **name**        | path  | string  | Ja           | Arbetsbokens filnamn.                                    |
| **sheetName**   | path  | string  | Ja           | Kalkylbladet som innehåller kolumnen.                    |
| **columnIndex** | path  | integer | Ja           | Nollbaserat index för kolumnen som ska hämtas.           |
| **folder**      | query | string  | Nej          | Lagringsmappen där arbetsboken finns.                    |
| **storageName** | query | string  | Nej          | Namnet på lagringstjänsten (t.ex. Aspose Cloud Storage). |

---

## cURL-exempel

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Svarsexempel

```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Svarschema

| Fält                | Typ     | Beskrivning                                          |
| ------------------- | ------- | ---------------------------------------------------- |
| `Column.GroupLevel` | integer | Grunderivnivå för kolumnen (används för gruppering). |
| `Column.Index`      | integer | Nollbaserat index för kolumnen.                      |
| `Column.IsHidden`   | boolean | `true` om kolumnen är dold, annars `false`.          |
| `Column.Width`      | number  | Kolumnens bredd uttryckt i tecken.                   |
| `Column.Style`      | object  | Innehåller en `link` till kolumnens stilresurs.      |
| `Column.link`       | object  | Självlänk till kolumnens resurs.                     |
| `Code`              | integer | HTTP-statuskod för svaret.                           |
| `Status`            | string  | Textuell beskrivning av statusen (t.ex. **OK**).     |

---

## Möjliga fel

| HTTP-status | Kod | Meddelande            | När det inträffar                                               |
| ----------- | --- | --------------------- | --------------------------------------------------------------- |
| 400         | 400 | Bad Request           | Saknas eller har felaktigt format för obligatoriska parametrar. |
| 401         | 401 | Unauthorized          | Saknas eller har ogiltig `Authorization`-header.                |
| 404         | 404 | Not Found             | Arbetsboken, kalkylbladet eller kolumnen finns inte.            |
| 500         | 500 | Internal Server Error | Oväntat serverproblem.                                          |

### Exempel – 404 Not Found

```json
{
  "Code": 404,
  "Message": "Kolumnindex utanför giltigt intervall."
}
```

### Exempel – 401 Unauthorized

```json
{
  "Code": 401,
  "Message": "Ogiltig eller saknad autentiseringstoken."
}
```

---

## SDK-exempel

Följande kodfragment visar hur du anropar operationen **Get Worksheet Columns** med hjälp av de officiella Aspose.Cells Cloud SDK:n. Om en Gist inte längre är tillgänglig finns exempelkoden även med direkt i dokumentet.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// Konfigurera API-klienten
var apiInstance = new CellsApi("client_id", "client_secret");

// Angivande av obligatoriska parametrar
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // valfritt
string storageName = "MyStorage";    // valfritt

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Kolumnindex: " + response.Column.Index);
    Console.WriteLine("Bredd: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Undantag vid anrop av CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // valfritt
        String storageName = "MyStorage";    // valfritt

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Kolumnindex: " + result.getColumn().getIndex());
            System.out.println("Bredd: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Undantag vid anrop av CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # valfritt
storage_name = "MyStorage"  # valfritt

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Kolumnindex:", response.column.index)
    print("Bredd:", response.column.width)
except Exception as e:
    print("Undantag vid anrop av CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
  clientId: "client_id",
  clientSecret: "client_secret",
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder"; // valfritt
const storageName = "MyStorage"; // valfritt

apiInstance
  .getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
  .then((result) => {
    console.log("Kolumnindex:", result.column?.index);
    console.log("Bredd:", result.column?.width);
  })
  .catch((error) => {
    console.error("Fel vid anrop av getWorksheetColumns:", error);
  });
```

</details>

> **Obs:** Alla SDK:n hanterar automatiskt `Authorization`-headern efter du har angett `client_id` och `client_secret`.

---

## Ytterligare resurser

- **OpenAPI-specifikation:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>
- **Autentiseringsguide:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **GitHub-repository (SDK:n och exempel):** <https://github.com/aspose-cells-cloud>

---

## _Dokumentet uppdaterades senast den 2026‑07‑30._