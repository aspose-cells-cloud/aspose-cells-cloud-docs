---
title: "Hämta radbeskrivning från ett Excel-arbetsblad"
second_title: "Document"
linktitle: "Row"
type: docs
url: /sv/rows/get/row/
aliases: [  /sv/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel-rad-API, Hämta arbetsbladsrad, REST-API, .NET SDK, Java SDK, Python SDK"
description: "Hämta detaljerad information (höjd, stil, dolt tillstånd etc.) för en specifik rad i ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, SDK-utdrag och felhantering."
weight: 10
ArticleTitle: "Hämta radbeskrivning från ett Excel-arbetsblad – Aspose.Cells Cloud API"
---

**Förutsättningar:**  
- Skaffa ett giltigt JWT-åtkomsttoken och inkludera det i `Authorization: Bearer <jwt token>`-headern.  
- Se till att arbetsboken är lagrad i Aspose Cloud-lagring eller ange mapp sökvägen där den finns.  
- Använd API-version **v3.0** som visas i slutpunkts-URL:en.

Denna REST API hämtar raddata baserat på dess index i ett Excel-arbetsblad.

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar**

| Parameter_name | Typ     | Plats  | Beskrivning                                         |
| -------------- | ------- | ------ | --------------------------------------------------- |
| name           | string  | path   | Namnet på arbetsbokens fil.                         |
| sheetName      | string  | path   | Namnet på arbetsbladet inom arbetsboken.            |
| rowIndex       | integer | path   | Noll-baserat index för raden som ska hämtas.        |
| folder         | string  | query  | Mappen som innehåller arbetsboken.                  |
| storageName    | string  | query  | Namnet på lagringen där arbetsboken finns.          |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL. Inkludera `Authorization: Bearer <jwt token>`-headern för att autentisera förfrågan.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Svarschema**

| Egenskap          | Typ     | Beskrivning                                                          |
|-------------------|---------|----------------------------------------------------------------------|
| `GroupLevel`      | integer | Utdragsnivå för raden (används för gruppering).                      |
| `Height`          | number  | Radhöjd i punkter.                                                   |
| `Index`           | integer | Noll-baserat index för den returnerade raden.                        |
| `IsBlank`         | boolean | Indikerar om raden innehåller någon data.                            |
| `IsHeightMatched`| boolean | `true` om radhöjden matchar standardhöjden för rader.               |
| `IsHidden`        | boolean | `true` om raden är dold.                                              |
| `Style`           | object  | Objekt som innehåller stilinformation för raden.                    |
| `link`            | object  | Hyperlänksreferens till radresursen.                                 |
| `Code`            | integer | HTTP-statuskod för svaret.                                           |
| `Status`          | string  | Textuell beskrivning av statusen (t.ex. “OK”).                      |

{{< /tab >}}

{{< /tabs >}}

**Anteckningar / Felhantering:** API:et kan returnera följande HTTP-statuskoder:

- **200** – Lyckades; raddata returneras.  
- **401** – Inte auktoriserad; JWT-token saknas eller är ogiltig.  
- **404** – Ej hittad; den angivna arbetsboken, arbetsbladet eller raden finns inte.  
- **500** – Internt serverfel; ett oväntat tillstånd uppstod.

| Kod  | Beskrivning                                   | Åtgärd                                    |
|------|-----------------------------------------------|-------------------------------------------|
| 200  | Lyckades – raddata returnerades.              | –                                         |
| 401  | Inte auktoriserad – saknad eller ogiltig JWT-token. | tillhandahåll en giltig JWT-token.        |
| 404  | Ej hittad – arbetsbok, arbetsblad eller rad saknas. | Kontrollera namn och radindex.           |
| 500  | Internt serverfel – oväntat tillstånd.        | Kontakta Aspose-support.                  |

För en komplett lista över felkoder, se Aspose.Cells Cloud [felkodsdokumentationen](https://docs.aspose.cloud/cells/).

## Cloud SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}