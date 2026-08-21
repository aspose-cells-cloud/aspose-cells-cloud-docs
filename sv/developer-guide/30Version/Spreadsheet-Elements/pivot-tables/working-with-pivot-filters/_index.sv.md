---
title: "Arbeta med pivotfilter"
second_title: "Dokument"
linktitle: Filter
type: docs
url: /sv/pivot-tables/add-filters/
aliases: [/sv/working-with-pivot-filters/]
keywords: "Aspose.Cells, Pivottabell, Filter, REST API, Molntjänst"
description: "Lär dig hur du lägger till, hämtar och tar bort pivottabellfilter med Aspose.Cells Cloud REST API. Innehåller begärandesyntax, nödvändiga parametrar, cURL-exempel och SDK-utdrag för C# och Go."
weight: 50
ArticleTitle: "Arbeta med pivotfilter – Aspose.Cells Cloud-dokumentation"
---

Denna REST API lägger till ett **pivotfilter** i pivottabellen vid angivet index.

**Förutsättningar**  
Innan du anropar denna slutpunkt måste du:

- Generera en giltig OAuth/JWT-åtkomsttoken och inkludera den i `Authorization`-headern.  
- Se till att målarboksen finns lagrad i en molnmapp som du har åtkomst till (ange `folder` och valfritt `storageName`).  
- Använd Aspose.Cells Cloud API version 3.0 eller senare.

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameter Name      | Typ     | Plats  | Beskrivning                                                                                     |
| ------------------- | ------- | ------ | ----------------------------------------------------------------------------------------------- |
| **name**            | string  | path   | Namnet på Excel-filen.                                                                          |
| **sheetName**       | string  | path   | Kalkylbladet som innehåller pivottabellen.                                                      |
| **pivotTableIndex** | integer | path   | Nollbaserat index för pivottabellen som filtret ska tillämpas på.                               |
| **filter**          | object  | body   | JSON-objekt som definierar filterinställningarna. Se tabellen **filter-schema** nedan.         |
| **needReCalculate** | boolean | query  | När **true** tvingas arbetsboken att oberäknas efter att filtret lagts till. Standard **false**. |
| **folder**          | string  | query  | Mapp i molnlagring där filen finns.                                                             |
| **storageName**     | string  | query  | Namn på molnlagringen.                                                                          |

**Filter-schema**

| Egenskap                     | Typ     | Beskrivning                                                                                 |
| ---------------------------- | ------- | ------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Inställningar för ett AutoFilter; kan utelämnas om ej används.                              |
| **EvaluationOrder**          | integer | Ordning enligt vilken filtret utvärderas.                                                    |
| **FieldIndex**               | integer | Nollbaserat index för det fält som filtret gäller.                                           |
| **FilterType**               | string  | Typ av filter (t.ex. `Value`, `Count`, `Label`).                                             |
| **MeasureFldIndex**          | integer | Index för mätfältet, om tillämpligt.                                                        |
| **MemberPropertyFieldIndex** | integer | Index för medlemsegenskapsfältet, om tillämpligt.                                            |
| **Name**                     | string  | Valfritt namn för filtret.                                                                   |
| **Value1**                   | string  | Första värdet som används av filtret (t.ex. undre gräns för ett intervall).                  |
| **Value2**                   | string  | Andra värdet som används av filtret (t.ex. övre gräns för ett intervall).                    |
| **CustomFilters**            | array   | Samling av anpassade filterobjekt (varje med `FilterOperatorType`, `Value1`, `Value2`).     |
| **DynamicFilter**            | object  | Inställningar för ett dynamiskt filter (t.ex. Top10, Bottom10).                              |
| **IconFilter**               | object  | Inställningar för ett ikonbaserat filter.                                                    |
| **Top10Filter**              | object  | Inställningar för ett Top10/Bottom10-filter.                                                 |
| **ColorFilter**              | object  | Inställningar för ett färgbaserat filter.                                                    |
| **Visibledropdown**          | boolean | Indikerar om filterlistrutan är synlig.                                                      |

> **Obs:** Alla ovanstående parametrar krävs om de inte uttryckligen är markerade som valfria i API-referensen.

### Svarskoder

| Kod | Betydelse                                    |
| --- | -------------------------------------------- |
| 200 | Filter tillagda framgångsrikt.              |
| 400 | Felaktig begäran – ogiltiga parametrar.      |
| 401 | Ej auktoriserad – saknad eller ogiltig token.|
| 404 | Ej hittad – arbetsbok eller pivottabell saknas. |
| 500 | Internt serverfel.                           |

**Bästa praxis**  
- Håll filterobjekt så små som möjligt; stora filterdefinitioner kan öka begärandefördröjningen.  
- Anrop är idempotenta – att lägga till samma filter två gånger skapar inte duplicerade poster.  
- Respektera API:s rate-limit på 100 begäranden per minut per konto.

*Ytterligare anteckningar:*  
- Den maximala storleken för en filterdefinition är 1 MB; större nyttolast kommer att avvisas med ett 400-fel.  
- När du använder `needReCalculate=true` kan ombereäkningen öka svartiden för stora arbetsböcker.

Du kan utforska den fullständiga OpenAPI-definitionen här:  
[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Exempel på cURL-begäran

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Molnsdk-familj

Att använda en SDK är det snabbaste sättet att utveckla mot Aspose.Cells Cloud. SDK:er hanterar detaljer på låg nivå, så att du kan fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // Initiera API-klienten (ersätt med dina autentiseringsuppgifter)
        var config = new Configuration
        {
            ClientId = "DIN_KLIENT_ID",
            ClientSecret = "DIN_KLIENT_HEMLIGHET"
        };
        var apiInstance = new CellsApi(config);

        // Bygg filterobjektet
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // Förbered begäran
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // Utför begäran
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Status: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

För ytterligare åtgärder relaterade till pivottabeller, se dokumentationen för **Lägg till**, **Ta bort** och **Rensa** filter.