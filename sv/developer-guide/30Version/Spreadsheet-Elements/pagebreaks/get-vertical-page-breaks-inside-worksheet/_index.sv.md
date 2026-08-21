---
title: "Hämta vertikala sidbrytningar"
second_title: "Dokument"
linktitle: "Hämta vertikala sidbrytningar"
type: docs
url: /sv/page-breaks/get-vertical-page-breaks/
aliases: [  /sv/get-vertical-page-breaks-inside-worksheet/ ]
keywords: "Aspose.Cells, vertikala sidbrytningar, Excel-API, molnbevakat kalkylark, REST-API"
description: "Hämta vertikala sidbrytningar från ett Excel-kalkylark med Aspose.Cells Cloud REST API (v3.0). Inkluderar HTTPS-slutpunkt, nödvändiga parametrar, cURL-exempel, svarsdetaljer, felhantering och SDK-exempel."
weight: 20
---

Denna REST API hämtar **vertikala** sidbrytningar från ett kalkylark.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Begärparametrar

| Parameternamn   | Typ    | Plats  | Beskrivning                                             | Nödvändig |
| --------------- | ------ | ------ | ------------------------------------------------------- | --------- |
| `name`          | string | path   | Namnet på Excel-filen.                                  | Ja        |
| `sheetName`     | string | path   | Namnet på kalkylarket från vilket brytningar ska läsas. | Ja        |
| `folder`        | string | query  | Mappen i lagringen som innehåller filen.                | Nej       |
| `storageName`   | string | query  | Namnet på Aspose Cloud-lagringen som ska användas.      | Nej       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Svarsdetaljer

| Fält                    | Typ   | Beskrivning                                                                                  |
| ----------------------- | ----- | -------------------------------------------------------------------------------------------- |
| `VerticalPageBreakList` | array | En samling objekt som representerar vertikala sidbrytningar.                                |
| `Column`                | int   | Kolumnindexet (nollbaserat) där brytningen sker.                                            |
| `StartRow`              | int   | Den första raden i brytningsintervallet (nollbaserat).                                      |
| `EndRow`                | int   | Den sista raden i brytningsintervallet (nollbaserat, vanligtvis `1048575` för sista raden). |
| `link.Href`             | string | URL som pekar på resursen själv (HTTPS).                                                    |
| `Code`                  | int   | HTTP-statuskod som returnerades av tjänsten.                                                |
| `Status`                | string | Textuell beskrivning av HTTP-statusen.                                                      |

### Felhantering

| HTTP-kod | Betydelse             | Vanlig orsak                                |
| -------- | --------------------- | ------------------------------------------- |
| 401      | Auktorisering saknas | Saknas eller ogiltigt JWT-token.            |
| 404      | Inte hittad           | Angiven fil eller kalkylark finns inte.     |
| 400      | Felaktig begäran      | Ogiltiga eller felaktiga frågeparametrar.   |
| 500      | Internt serverfel     | Oväntat tillstånd på serversidan.           |

Kontrollera fälten `Code` och `Status` i JSON-svaret för ytterligare detaljer.

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla mot Aspose.Cells Cloud. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}