---
title: "Sök text i Excel-filer – Aspose.Cells Cloud API"
description: "Sök efter specifik text i Excel-filer (XLS, XLSX, XLSM, XLSB) och ODS-filer med Aspose.Cells Cloud API. Inkluderar begärandedetaljer, cURL- och SDK-exempel samt felhantering."
keywords: "Aspose.Cells, Excel, sök, API, REST"
type: docs
url: /sv/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Sök text i Excel-filer – Aspose.Cells Cloud API

## Översikt
Aspose.Cells Cloud tillhandahåller en **POST**-ändpunkt som söker efter en given textsträng i Excel-arbetsböcker (XLS, XLSX, XLSM, XLSB) och OpenDocument-kalkylark (ODS-filer). API:t returnerar varje cell som innehåller den sökta texten tillsammans med en länk till det kalkylblad där träffen hittades.

> **Användningsfall**  
> - Verifiera att ett visst värde finns i en rapport innan vidare bearbetning sker.  
> - Bygg ett snabbt "sök-och-ersätt"-verktyg som först listar alla förekomster.  
> - Skapa ett index över nyckelord över ett antal kalkylblad.

---

## Förutsättningar
| Krav | Detaljer |
|------|----------|
| **Autentisering** | JWT-token som erhålls via Aspose Cloud OAuth-flödet. Token måste inkludera **Cells**-omfattningen. |
| **Stödda format** | XLS, XLSX, XLSM, XLSB, ODS |
| **Maximal filstorlek** | 150 MB (komprimerad). Större filer returnerar **413 Payload Too Large**. |
| **Nödvändiga headrar** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **Behörigheter** | Token måste ha *läs*-behörighet på mål-lagringen (vid användning av fjärrlagring) – ej nödvändig när filen laddas upp som `multipart/form-data`. |

*Tips:* Använd **/connect/token**-ändpunkten för att generera en JWT-token. Se [Autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) för detaljer.

---

## Ändpunkt

| Objekt | Värde |
|--------|-------|
| **HTTP-metod** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **Syfte** | Sök efter angiven text i en uppladdad Excel-arbetsbok. |
| **Säkerhet** | JWT-token (Bearer) – se *Förutsättningar* ovan. |

---

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## Begärandeparametrar

| Namn | Typ | Plats | Nödvändig | Beskrivning |
|------|-----|-------|-----------|-------------|
| `file` | **fil** | `formData` (multipart) | **Ja** | Kalkylbladsfilen som ska laddas upp. |
| `text` | **sträng** | Frågesträng | **Ja** | Textsträngen som ska sökas efter. |
| `password` | **sträng** | Frågesträng | Nej | Lösenord för öppnande av ett lösenordsskyddat kalkylblad, vid behov. |
| `sheetname` | **sträng** | Frågesträng | Nej | Namn på kalkylbladet som sökningen ska begränsas till. Om utelämnas söks alla kalkylblad. |
| `checkExcelRestriction` | **boolean** | Frågesträng | Nej (standard: `true`) | När `true` validerar API:t Excel-specifika begränsningar (t.ex. skrivskyddade celler) innan sökning sker. |

---

## Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*Ersätt `<jwt-token>` med en giltig token och justera frågeparametrarna enligt behov.*

---

## Lyckad respons

**HTTP 200 – Sökningen lyckades; responsen innehåller hittade textobjekt.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Responsfält

| Fält | Typ | Beskrivning |
|------|-----|-------------|
| `Status` | sträng | Övergripande begäranstatus (`OK` för lyckad begäran). |
| `Code` | heltal | HTTP-statuskod (200). |
| `TextItems.link` | objekt | Hypermedial länk till samlingresursen. |
| `TextItems.TextItemList` | array | Lista över träffar. Varje objekt innehåller: |
| `Text` | sträng | Cellvärdet som matchade söktexten. |
| `link` | objekt | Hyperlänk till kalkylbladet där träffen hittades (`Href` pekar på `Workbook/worksheets/SheetName`). |

---

## Felresponser

| HTTP-kod | Betydelse | Vanlig orsak | Exempel på body |
|----------|-----------|--------------|-----------------|
| **400** | Bad Request | Saknade nödvändiga parametrar, icke-stött filformat eller ogiltiga frågevärden. | `{ "Status":"Error","Code":400,"Message":"The 'text' query parameter is required." }` |
| **401** | Unauthorized | Saknad eller ogiltig JWT-token. | `{ "Status":"Error","Code":401,"Message":"Invalid or expired access token." }` |
| **413** | Payload Too Large | Uppladdad fil överskrider 150 MB-gränsen. | `{ "Status":"Error","Code":413,"Message":"File size exceeds the allowed limit." }` |
| **500** | Internal Server Error | Oväntat serverproblem. | `{ "Status":"Error","Code":500,"Message":"An unexpected error occurred." }` |

---

## SDK-exempel

Här nedan finns minimala kodstycken för **PostSearch**-åtgärden med de officiella Aspose.Cells Cloud SDK:n. Ersätt `YOUR_JWT_TOKEN` och filsökvägen med egna värden.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(SDK för PHP, Ruby, Go och Perl finns tillgängliga i [Aspose.Cells Cloud GitHub-repositoriet](https://github.com/aspose-cells-cloud).)*

---

## Ytterligare anteckningar

- **`checkExcelRestriction`** är `true` som standard. Ställ in till `false` endast om du är säker på att arbetsboken inte innehåller skyddade celler som kan störa sökningen.
- API:t returnerar **hypermediala länkar** (`Href`) som kan användas med andra Aspose.Cells-ändpunkter (t.ex. för att ladda ner kalkylbladet eller hämta cellformatering).
- Vid sökning i stora arbetsböcker kan du förbättra svarstiden genom att begränsa omfattningen med `sheetname`-parametern.

---

## Relaterade länkar

- **Autentiseringsguide** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **OpenAPI-specifikation för PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDK:n** – <https://github.com/aspose-cells-cloud>
- **Begränsningar och kvoter** – <https://docs.aspose.cloud/total/getting-started/limits/>

---