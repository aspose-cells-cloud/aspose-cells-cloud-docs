---
title: "Hämta sidantal för ett Excel-kalkylblad"
second_title: "Dokument"
linktitle: "PageCount"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, Excel API, kalkylbladets sidantal, REST, molntjänst, Excel-paginering"
description: "Hämta antalet utskriftbara sidor i ett Excel-kalkylblad med Aspose.Cells Cloud REST API (v3.0). Inkluderar HTTPS-begäranformat, autentiseringssteg, exempel på cURL, fullständig JSON-svar, statuskoder och SDK-kodexempel."
weight: 10
ArticleTitle: "Hämta sidantal för ett Excel-kalkylblad – Aspose.Cells Cloud API"
---

Denna REST API returnerar **sidantalet** för ett kalkylblad.

**Autentisering:** Alla Aspose.Cells Cloud-slutpunkter kräver en Bearer-token som erhålls via OAuth2-flödet. Inkludera token i `Authorization`-huvudet enligt exemplified i cURL-exemplet nedan.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### Begärandeparametrar

| Parameter   | Typ    | Plats  | Beskrivning                               |
| ----------- | ------ | ------ | ----------------------------------------- |
| name        | string | path   | Dokumentets namn.                         |
| sheetName   | string | path   | Kalkylbladets namn.                       |
| folder      | string | query  | Mapp som innehåller dokumentet.           |
| storageName | string | query  | Namn på lagringsutrymmet.                 |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Exemplet nedan visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Svarsdetaljer

| HTTP-status | Betydelse                                         |
| ----------- | ------------------------------------------------- |
| **200**     | Lyckades – returnerar JSON-svaret ovan.           |
| **401**     | Oauktoriserad – token saknas eller är ogiltig.    |
| **404**     | Hittades inte – filen eller kalkylbladet finns inte. |
| **500**     | Internt serverfel – oväntat serverfel.            |

### Versionshistorik

_API-version **v3.0** (släppt 2025). Om du använder en nyare version, hänvisa till den uppdaterade slutpunktsdokumentationen._

## Molntjänstfamilj (SDK)

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Anteckningar

- Sidantalet speglar utskriftslayouten och tar hänsyn till sidbrytningar, marginaler och skalning. Dolda rader eller kolumner kan påverka resultatet.
- Se till att målkalkylbladet finns och att filen är lagrad i den angivna `folder` och `storageName` innan du gör begäran.