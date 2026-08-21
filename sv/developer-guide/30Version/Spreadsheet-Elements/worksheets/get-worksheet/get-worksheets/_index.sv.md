---
title: "Hämta alla kalkylblad"
second_title: "Document"
linktitle: "Alla"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, molntjänst, hämta kalkylblad, Excel, REST, SDK"
description: "Hämta listan över kalkylblad i en Excel-arbetsbok via Aspose.Cells Cloud REST API (v3.0). Inkluderar cURL-exempel, SDK-utdrag och svarsschema."
weight: 10
---

Denna REST API returnerar information om kalkylbladen som finns i en arbetsbok.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Förfrågningsparametrar**

| Parametername   | Typ    | Plats  | Beskrivning                              |
| --------------- | ------ | ------ | ---------------------------------------- |
| name            | string | path   | Namnet på Excel-dokumentet.              |
| folder          | string | query  | Mappen som innehåller dokumentet.        |
| storageName     | string | query  | Namnet på den lagring som ska användas.  |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att komma åt Aspose.Cells Cloud-tjänster. Exemplet nedan visar en GET-förfrågan för att hämta kalkylbladen.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Felhantering

Typiska HTTP-statuskoder som returneras av detta slutställe:

| Kod | Betydelse              | Beskrivning                                |
| --- | ---------------------- | ------------------------------------------ |
| 400 | Felaktig förfrågan     | Saknar nödvändig parameter (t.ex. `name`). |
| 401 | Auktorisering saknas   | Ogiltigt eller saknat JWT-token.           |
| 404 | Hittades inte          | Angiven arbetsbok finns inte.              |
| 500 | Internt serverfel      | Oväntat serverfel.                         |

Felsvar returneras i JSON-format, till exempel:

```json
{
  "Code": "401",
  "Message": "Invalid access token."
}
```

## Molnsdk-familj

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-repositoryt](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}