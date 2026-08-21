---
title: Lägg till en dynamisk filter i ett Excel-ark med Aspose.Cells Cloud API
description: Lär dig hur du tillämpar ett dynamiskt filter (t.ex. BelowAverage, Tomorrow, LastMonth) på ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar autentisering, begäranssyntax, parametrar, svarshantering och SDK-exempel för flera språk.
keywords: Aspose.Cells, dynamiskt filter, Excel API, REST, autofilter, moln-SDK
slug: add-dynamic-filter
api_version: v3.0
---

## Översikt

**PutWorksheetDynamicFilter**-åtgärden lägger till ett dynamiskt filter i ett angivet område i ett Excel-ark.  
Dynamiska filter utvärderar automatiskt värden såsom datum, medelvärden eller tomma celler, vilket gör att du kan skapa "smart" vyer utan att skriva anpassade formler.

## Förutsättningar

| Krav | Detaljer |
|------|----------|
| **Autentisering** | En giltig JWT-token som erhålls från `/connect/token`-slutpunkten. Inkludera den i `Authorization: Bearer <token>`-headern. |
| **Lagring** | Arbetsboken måste finnas i en Aspose Cloud-lagringsplats (standard eller anpassad lagring). |
| **Stödda filformat** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv`, etc. |
| **Behörigheter** | Läs/skriv-åtkomst till målmappen/filen. |

## HTTP-begäran

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Sökvägsparametrar

| Parameter | Typ | Krävs | Beskrivning |
|-----------|-----|-------|-------------|
| `name` | string | ✅ | Namnet på Excel-arbetsboken (t.ex. `Book1.xlsx`). |
| `sheetName` | string | ✅ | Namnet på arbetsarket som innehåller det område som ska filtreras. |

### Frågeparametrar

| Parameter | Typ | Krävs | Beskrivning |
|-----------|-----|-------|-------------|
| `range` | string | ✅ | Cellområdet där filtret tillämpas (t.ex. `A1:B1`). |
| `fieldIndex` | integer | ✅ | Nollbaserat kolumnindex i området där det dynamiska filtret tillämpas. |
| `dynamicFilterType` | string | ✅ | Typ av dynamiskt filter att tillämpa (se **Stödda dynamiska filtertyper**). |
| `matchBlanks` | boolean | ❌ | Om `true` ingår tomma celler i filterresultaten. Standard: `false`. |
| `refresh` | boolean | ❌ | Om `true` uppdateras autofiltret efter att filtret tillämpats. |
| `folder` | string | ❌ | Sökvägen till mappen i lagringen där arbetsboken finns. |
| `storageName` | string | ❌ | Namnet på Aspose Cloud-lagringen som ska användas. |

### Begärandetext

Begärandetexten är ett tomt JSON-objekt:

```json
{}
```

## Stödda dynamiska filtertyper

| Värde | Betydelse |
|-------|-----------|
| `BelowAverage` | Rader vars värde är under kolumnens medelvärde. |
| `AboveAverage` | Rader vars värde är över kolumnens medelvärde. |
| `Tomorrow` | Rader med datum som motsvarar imorgon. |
| `Yesterday` | Rader med datum som motsvarar igår. |
| `NextWeek` | Rader med datum som ligger i nästa kalendervecka. |
| `LastMonth` | Rader med datum från föregående månad. |
| `ThisYear` | Rader med datum som inträffar i det aktuella året. |

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT-begäran har en tom JSON-begärandetext
```

## Exempel på svar

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Dynamiskt filter har tillämpats framgångsrikt."
}
```

**HTTP-statuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Filter har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran | Saknade eller ogiltiga parametrar (t.ex. filformat som inte stöds). |
| 401 | Autentisering krävs | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel | Oväntat serverfel. |

## SDK-exempel

Nedan finns klara att köra kodsnuttar för de mest populära SDK:erna. Ersätt `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` och andra platshållare med dina faktiska värden.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | Namnet på arbetsboken.
var sheetName = "Sheet1"; // string | Namnet på arbetsarket.
var range = "A1:B1"; // string | Området att filtrera.
var fieldIndex = 0; // int? | Nollbaserat kolumnindex.
var dynamicFilterType = "BelowAverage"; // string | Typ av dynamiskt filter.
var matchBlanks = true; // bool? | Inkludera tomma celler.
var refresh = true; // bool? | Uppdatera efter tillämpning.
var folder = "myFolder"; // string (valfritt)
var storageName = null; // string (valfritt)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Undantag vid anrop av AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (valfritt)
            undefined              // storageName (valfritt)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Liknande kodsnuttar finns tillgängliga för Ruby, PHP, Go och Perl i det officiella SDK-repositoriet.)*

## Relaterade ämnen

- **Lägg till ett standardautofilter** – [Lägg till ett standardfilter](/autofilter/add-filter)  
- **Lägg till ett datumfilter** – [Lägg till ett datumfilter](/autofilter/add-date-filter)  
- **Ta bort ett autofilter** – [Ta bort autofilter](/autofilter/delete-filter)  
- **Arbeta med arbetsark** – [Översikt över arbetsark-API](/worksheets/)

## Anteckningar

* Alla bilder som används i den ursprungliga dokumentationen har granskats för tillgänglighet. Dekorative ikoner är märkta med `alt=""` och `role="presentation"`; funktionella ikoner behåller beskrivande `alt`-texter.  
* Meta-nyckelord har rensats för att ta bort tomma poster och dubbletter.  
* Sidan följer nu en tydlig rubrikhierarki (en enda H1 i front matter, H2 för huvudavsnitt, H3/H4 för underavsnitt) för att förbättra SEO och skärmläsarnavigering.